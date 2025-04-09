#tirthprajapati

import { useState } from 'react';
import { Card, CardContent } from '@/components/ui/card';
import { Button } from '@/components/ui/button';
import { Tabs, TabsList, TabsTrigger, TabsContent } from '@/components/ui/tabs';

export default function Portfolio() {
  const [selectedTab, setSelectedTab] = useState('about');

  return (
    <div className="min-h-screen bg-gradient-to-br from-blue-50 via-purple-100 to-pink-50 p-6 font-sans">
      <div className="max-w-5xl mx-auto bg-white bg-opacity-70 rounded-2xl shadow-2xl p-8">
        <h1 className="text-4xl font-extrabold text-purple-800 mb-2 text-center">Tirth Prajapati</h1>
        <p className="mb-6 text-gray-700 text-center">Visual Merchandiser | Retail Strategist | Marketing Coordinator</p>

        <Tabs value={selectedTab} onValueChange={setSelectedTab} className="mb-6">
          <TabsList className="flex justify-center gap-2 bg-purple-100 rounded-xl p-2">
            <TabsTrigger value="about">About</TabsTrigger>
            <TabsTrigger value="experience">Experience</TabsTrigger>
            <TabsTrigger value="education">Education</TabsTrigger>
            <TabsTrigger value="skills">Skills</TabsTrigger>
            <TabsTrigger value="projects">VM Projects</TabsTrigger>
            <TabsTrigger value="contact">Contact</TabsTrigger>
          </TabsList>

          <TabsContent value="about">
            <Card className="bg-gradient-to-br from-pink-100 to-purple-50">
              <CardContent className="p-6">
                <p className="text-gray-800">
                  Creative and data-driven professional with 3+ years in visual merchandising, retail operations, and marketing.
                  Proven record in crafting compelling brand stories and optimizing store layouts for performance.
                </p>
              </CardContent>
            </Card>
          </TabsContent>

          <TabsContent value="experience">
            <Card className="bg-white shadow-md">
              <CardContent className="p-6 space-y-4">
                <div>
                  <h3 className="font-bold text-lg text-purple-700">Amazon – Process Management Associate</h3>
                  <p className="text-sm text-gray-500">Burnaby, Canada | Aug 2022 – Present</p>
                  <ul className="list-disc ml-5 text-sm text-gray-700">
                    <li>99%+ inventory accuracy, bottleneck resolution, OSHA compliance</li>
                    <li>Trained new hires and improved onboarding efficiency</li>
                  </ul>
                </div>
                <div>
                  <h3 className="font-bold text-lg text-purple-700">Westside – Men’s Buyer & Visual Merchandiser</h3>
                  <p className="text-sm text-gray-500">Ahmedabad, India | Jun 2020 – Jul 2021</p>
                  <ul className="list-disc ml-5 text-sm text-gray-700">
                    <li>Increased sales by 15% YoY via strong merchandising strategy</li>
                    <li>Visual displays and vendor negotiations for improved margins</li>
                  </ul>
                </div>
                <div>
                  <h3 className="font-bold text-lg text-purple-700">Aspire Edusoft – Marketing Project Manager</h3>
                  <p className="text-sm text-gray-500">Remote | Feb 2023 – Aug 2024</p>
                  <ul className="list-disc ml-5 text-sm text-gray-700">
                    <li>Led client projects, trained teams, secured clients like Trulioo</li>
                  </ul>
                </div>
              </CardContent>
            </Card>
          </TabsContent>

          <TabsContent value="education">
            <Card className="bg-purple-50">
              <CardContent className="p-6 space-y-3 text-purple-900">
                <p><strong>MBA – Marketing & Sales</strong><br/>University Canada West, Vancouver | 2022 – 2023</p>
                <p><strong>BA – Literature & Psychology (Gold Medalist)</strong><br/>Gujarat University, India | 2018 – 2021</p>
                <p><strong>Certifications</strong><br/>International Marketing, Design Thinking, Google UI/UX, PMI (in progress)</p>
              </CardContent>
            </Card>
          </TabsContent>

          <TabsContent value="skills">
            <Card className="bg-pink-100">
              <CardContent className="p-6 grid grid-cols-2 gap-3 text-sm text-gray-800">
                <span>Visual Merchandising</span>
                <span>Inventory Management</span>
                <span>Marketing Coordination</span>
                <span>Customer Engagement</span>
                <span>CRM (Smart Assist, Oracle)</span>
                <span>Excel, Outlook, Tableau, CAD</span>
                <span>Team Leadership</span>
                <span>Multilingual: English, Hindi, Gujarati</span>
              </CardContent>
            </Card>
          </TabsContent>

          <TabsContent value="projects">
            <Card className="bg-gradient-to-br from-purple-50 to-pink-100">
              <CardContent className="p-6 space-y-4">
                <div>
                  <h4 className="font-semibold text-purple-800">Winter 2020 – Urban Explorer</h4>
                  <p className="text-sm text-gray-700">Theme-based VM with jackets and boots. Led to 12% sales lift in category.</p>
                </div>
                <div>
                  <h4 className="font-semibold text-purple-800">Summer Sale 2021 – Clearance Optimization</h4>
                  <p className="text-sm text-gray-700">Designed impulse zones, signage layouts, reducing excess inventory by 18%.</p>
                </div>
                <div>
                  <h4 className="font-semibold text-purple-800">Storefront July 2021 – Monochrome Mix</h4>
                  <p className="text-sm text-gray-700">Color-blocking VM strategy aligning with new season launch visuals.</p>
                </div>
              </CardContent>
            </Card>
          </TabsContent>

          <TabsContent value="contact">
            <Card className="bg-white shadow-lg">
              <CardContent className="p-6 text-sm text-gray-700">
                <p><strong>Email:</strong> tirthprajapati00@gmail.com</p>
                <p><strong>Phone:</strong> 236-989-1599</p>
                <p><strong>Location:</strong> Vancouver, BC</p>
                <p><strong>Availability:</strong> Open for full-time roles in merchandising, marketing, or operations</p>
              </CardContent>
            </Card>
          </TabsContent>
        </Tabs>
      </div>
    </div>
  );
}
