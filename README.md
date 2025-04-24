import React from "react"; import { Card, CardContent } from "@/components/ui/card"; import { Button } from "@/components/ui/button"; import { Input } from "@/components/ui/input"; import { Textarea } from "@/components/ui/textarea"; import { CalendarIcon } from "lucide-react";

export default function AppointmentPage() { return ( <div className="min-h-screen bg-gradient-to-br from-indigo-500 to-purple-600 flex items-center justify-center p-6"> <Card className="w-full max-w-2xl shadow-2xl rounded-2xl bg-white/90 backdrop-blur p-6"> <CardContent> <h1 className="text-3xl font-bold text-center text-indigo-700 mb-6"> Book Your Appointment </h1> <form 
action="https://formsubmit.co/kaifsiddiquibth@gmail.com" 
method="POST" 
className="space-y-4"
> {/* Hidden inputs to configure Formsubmit */} <input type="hidden" name="_captcha" value="false" /> <input type="hidden" name="_template" value="table" /> <input type="hidden" name="_autoresponse" value="Thank you for booking your appointment! We will contact you shortly." />

<Input placeholder="Full Name" name="name" required className="bg-white/80" />
        <Input placeholder="Phone Number" name="phone" required type="tel" className="bg-white/80" />
        <Input type="email" placeholder="Email Address" name="email" className="bg-white/80" />
        <div className="flex items-center space-x-2">
          <Input type="date" name="date" className="bg-white/80 flex-1" />
          <Input type="time" name="time" className="bg-white/80 w-32" />
          <CalendarIcon className="text-indigo-500" />
        </div>
        <Textarea placeholder="Message (optional)" name="message" className="bg-white/80" />
        <Button type="submit" className="w-full bg-indigo-600 hover:bg-indigo-700 text-white font-semibold py-2 rounded-xl transition-all duration-200">
          Confirm Appointment
        </Button>
      </form>
    </CardContent>
  </Card>
</div>

); }

