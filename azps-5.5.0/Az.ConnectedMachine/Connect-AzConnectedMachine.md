---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/connect-azconnectedmachine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Connect-AzConnectedMachine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Connect-AzConnectedMachine.md
ms.openlocfilehash: 281d456eb7612914bac546b3d361238bb5056626
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243997"
---
# <span data-ttu-id="9af51-101">Connect-AzConnectedMachine</span><span class="sxs-lookup"><span data-stu-id="9af51-101">Connect-AzConnectedMachine</span></span>

## <span data-ttu-id="9af51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9af51-102">SYNOPSIS</span></span>
<span data-ttu-id="9af51-103">API для регистрации нового компьютера и создания отслеживаемго ресурса в ARM</span><span class="sxs-lookup"><span data-stu-id="9af51-103">API to register a new machine and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="9af51-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9af51-104">SYNTAX</span></span>

```
Connect-AzConnectedMachine [-ResourceGroupName] <String> [-Location] <String> [[-SubscriptionId] <String>]
 [[-Name] <String>] [[-DefaultProfile] <PSObject>] [[-PSSession] <PSSession[]>] [[-Tag] <Hashtable>]
 [[-Proxy] <Uri>] [<CommonParameters>]
```

## <span data-ttu-id="9af51-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9af51-105">DESCRIPTION</span></span>
<span data-ttu-id="9af51-106">API для регистрации нового компьютера и создания отслеживаемго ресурса в ARM</span><span class="sxs-lookup"><span data-stu-id="9af51-106">API to register a new machine and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="9af51-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9af51-107">EXAMPLES</span></span>

### <span data-ttu-id="9af51-108">Пример 1. Подключение компьютера, на который вы подключены,</span><span class="sxs-lookup"><span data-stu-id="9af51-108">Example 1: Onboards the machine you're on as a connected machine</span></span>
```powershell
PS C:\> Connect-AzConnectedMachine -ResourceGroupName contoso-connected-machines -Name linux_eastus1_1 -Location eastus

< truncated output of installing the azcmagent >

time="2020-08-07T13:13:25-07:00" level=info msg="Onboarding Machine. It usually takes a few minutes to complete. Sometimes it may take longer depending on network and server load status."
time="2020-08-07T13:13:25-07:00" level=info msg="Check network connectivity to all endpoints..."
time="2020-08-07T13:13:29-07:00" level=info msg="All endpoints are available... continue onboarding"
time="2020-08-07T13:13:50-07:00" level=info msg="Successfully Onboarded Resource to Azure" VM Id=978ab182-6cf0-4de3-a58b-53c8d0a3235e

Name             Location OSName   Status     ProvisioningState
----             -------- ------   ------     -----------------
linux_eastus1_1  eastus   linux    Connected  Succeeded
```

<span data-ttu-id="9af51-109">Передает компьютер, на который вы подключены, как подключенный компьютер.</span><span class="sxs-lookup"><span data-stu-id="9af51-109">Onboards the machine you're on as a connected machine.</span></span>

### <span data-ttu-id="9af51-110">Пример 2. Подключение удаленного компьютера к подключению</span><span class="sxs-lookup"><span data-stu-id="9af51-110">Example 2: Onboards a remote machine as a connected device</span></span>
```powershell
PS C:\> $session = Connect-PSSession -ComputerName WINBOX
PS C:\> Connect-AzConnectedMachine -ResourceGroupName contoso-rg -Name win_eastus1_1 -Location eastus -PSSession $session

< truncated output of installing the azcmagent >

time="2020-08-07T13:13:25-07:00" level=info msg="Onboarding Machine. It usually takes a few minutes to complete. Sometimes it may take longer depending on network and server load status."
time="2020-08-07T13:13:25-07:00" level=info msg="Check network connectivity to all endpoints..."
time="2020-08-07T13:13:29-07:00" level=info msg="All endpoints are available... continue onboarding"
time="2020-08-07T13:13:50-07:00" level=info msg="Successfully Onboarded Resource to Azure" VM Id=978ab182-6cf0-4de3-a58b-53c8d0a3236a

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
win_eastus1_1  eastus   windows  Connected  Succeeded
```

<span data-ttu-id="9af51-111">Передает удаленный компьютер в качестве подключенного устройства с помощью переемирования PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9af51-111">Onboards a remote machine as a connected device using PowerShell remoting.</span></span>
<span data-ttu-id="9af51-112">Примечание. В настоящее время поддерживается только Windows в качестве целевого.</span><span class="sxs-lookup"><span data-stu-id="9af51-112">Note: only Windows as the target is supported at this time.</span></span>

## <span data-ttu-id="9af51-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9af51-113">PARAMETERS</span></span>

### <span data-ttu-id="9af51-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9af51-114">-DefaultProfile</span></span>
<span data-ttu-id="9af51-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9af51-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9af51-116">-Location</span><span class="sxs-lookup"><span data-stu-id="9af51-116">-Location</span></span>
<span data-ttu-id="9af51-117">Расположение созданной подключеннойMa ветви.</span><span class="sxs-lookup"><span data-stu-id="9af51-117">The location for the created ConnectedMachine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9af51-118">-Name</span><span class="sxs-lookup"><span data-stu-id="9af51-118">-Name</span></span>
<span data-ttu-id="9af51-119">Имя, которое будет использоваться для этого компьютера.</span><span class="sxs-lookup"><span data-stu-id="9af51-119">The name that will be used for this machine.</span></span>
<span data-ttu-id="9af51-120">По умолчанию используется имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="9af51-120">The hostname is used by default.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9af51-121">-Прокси-сервер</span><span class="sxs-lookup"><span data-stu-id="9af51-121">-Proxy</span></span>
<span data-ttu-id="9af51-122">URI используемой прокси-сервера</span><span class="sxs-lookup"><span data-stu-id="9af51-122">The URI for the proxy server to use</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9af51-123">-PSSession</span><span class="sxs-lookup"><span data-stu-id="9af51-123">-PSSession</span></span>
<span data-ttu-id="9af51-124">При этом команда, которая передает компьютеры в Azure, будет запускаться в рамках каждого PSSession.</span><span class="sxs-lookup"><span data-stu-id="9af51-124">When specified, the command that onboards machines to Azure will be run within each PSSession.</span></span>
<span data-ttu-id="9af51-125">ПРИМЕЧАНИЕ. В настоящее время это работает только в Windows.</span><span class="sxs-lookup"><span data-stu-id="9af51-125">NOTE: This only works on Windows for now.</span></span>

```yaml
Type: System.Management.Automation.Runspaces.PSSession[]
Parameter Sets: (All)
Aliases: Session

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9af51-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9af51-126">-ResourceGroupName</span></span>
<span data-ttu-id="9af51-127">Имя группы ресурсов, в которая вы хотите добавить компьютер.</span><span class="sxs-lookup"><span data-stu-id="9af51-127">The name of the resource group you want to add the machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9af51-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9af51-128">-SubscriptionId</span></span>
<span data-ttu-id="9af51-129">ИД подписки, в который вы хотите добавить компьютер.</span><span class="sxs-lookup"><span data-stu-id="9af51-129">The ID of the subscription you want to add the machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9af51-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="9af51-130">-Tag</span></span>
<span data-ttu-id="9af51-131">Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9af51-131">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9af51-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9af51-132">CommonParameters</span></span>
<span data-ttu-id="9af51-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9af51-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9af51-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9af51-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9af51-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9af51-135">INPUTS</span></span>

## <span data-ttu-id="9af51-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9af51-136">OUTPUTS</span></span>

## <span data-ttu-id="9af51-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9af51-137">NOTES</span></span>

<span data-ttu-id="9af51-138">ALIASES</span><span class="sxs-lookup"><span data-stu-id="9af51-138">ALIASES</span></span>

## <span data-ttu-id="9af51-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9af51-139">RELATED LINKS</span></span>

