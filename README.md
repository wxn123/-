# 实验一python代码

    def __init__( self ):
        "Create custom topo."

        # Initialize topology
        Topo.__init__( self )

        # Add hosts and switches
        H1 = self.addHost( 'h1' )
        H2 = self.addHost( 'h2' )
	H3 = self.addHost( 'h3' )
	H4 = self.addHost( 'h4' )
	H5 = self.addHost( 'h5' )
	H6 = self.addHost( 'h6' )
	H7 = self.addHost( 'h7' )
	H8 = self.addHost( 'h8' )
        S4 = self.addSwitch( 's4' )
        S5 = self.addSwitch( 's5' )
	S6 = self.addSwitch( 's6' )
	S7 = self.addSwitch( 's7' )
	S2 = self.addSwitch( 's2' )
	S3 = self.addSwitch( 's3' )
	S1 = self.addSwitch( 's1' )

        # Add links
        self.addLink( H1, S4 )
        self.addLink( S4, H2 )
        self.addLink( S4, S2 )
	self.addLink( S2, S5 )
	self.addLink( H3, S5 )
	self.addLink( S5, H4 )
	self.addLink( S2, S1 )
	self.addLink( S1, S3 )
	self.addLink( S3, S6 )
	self.addLink( H5, S6 )
	self.addLink( S6, H6 )
	self.addLink( S3, S7 )
	self.addLink( H7, S7 )
	self.addLink( S7, H8 )
topos = { 'mytopo': ( lambda: MyTopo() ) }
