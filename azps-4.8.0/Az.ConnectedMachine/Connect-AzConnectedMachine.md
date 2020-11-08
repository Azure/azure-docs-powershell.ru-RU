---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/connect-azconnectedmachine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Connect-AzConnectedMachine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Connect-AzConnectedMachine.md
ms.openlocfilehash: 281d456eb7612914bac546b3d361238bb5056626
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079776"
---
# <span data-ttu-id="91273-101">Connect-AzConnectedMachine</span><span class="sxs-lookup"><span data-stu-id="91273-101">Connect-AzConnectedMachine</span></span>

## <span data-ttu-id="91273-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="91273-102">SYNOPSIS</span></span>
<span data-ttu-id="91273-103">API для регистрации нового компьютера и, таким образом, для создания отслеживаемого ресурса на ARM</span><span class="sxs-lookup"><span data-stu-id="91273-103">API to register a new machine and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="91273-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="91273-104">SYNTAX</span></span>

```
Connect-AzConnectedMachine [-ResourceGroupName] <String> [-Location] <String> [[-SubscriptionId] <String>]
 [[-Name] <String>] [[-DefaultProfile] <PSObject>] [[-PSSession] <PSSession[]>] [[-Tag] <Hashtable>]
 [[-Proxy] <Uri>] [<CommonParameters>]
```

## <span data-ttu-id="91273-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="91273-105">DESCRIPTION</span></span>
<span data-ttu-id="91273-106">API для регистрации нового компьютера и, таким образом, для создания отслеживаемого ресурса на ARM</span><span class="sxs-lookup"><span data-stu-id="91273-106">API to register a new machine and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="91273-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="91273-107">EXAMPLES</span></span>

### <span data-ttu-id="91273-108">Пример 1: встроенный компьютер в качестве подключенного компьютера</span><span class="sxs-lookup"><span data-stu-id="91273-108">Example 1: Onboards the machine you're on as a connected machine</span></span>
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

<span data-ttu-id="91273-109">Интегрированный компьютер, на котором установлен подключенный компьютер.</span><span class="sxs-lookup"><span data-stu-id="91273-109">Onboards the machine you're on as a connected machine.</span></span>

### <span data-ttu-id="91273-110">Пример 2: подключение удаленного компьютера к подключенному устройству</span><span class="sxs-lookup"><span data-stu-id="91273-110">Example 2: Onboards a remote machine as a connected device</span></span>
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

<span data-ttu-id="91273-111">Настольная плата на удаленном компьютере в качестве подключенного устройства с помощью удаленного взаимодействия PowerShell.</span><span class="sxs-lookup"><span data-stu-id="91273-111">Onboards a remote machine as a connected device using PowerShell remoting.</span></span>
<span data-ttu-id="91273-112">Примечание. в настоящее время поддерживается только Windows в качестве целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="91273-112">Note: only Windows as the target is supported at this time.</span></span>

## <span data-ttu-id="91273-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="91273-113">PARAMETERS</span></span>

### <span data-ttu-id="91273-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91273-114">-DefaultProfile</span></span>
<span data-ttu-id="91273-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="91273-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91273-116">-Location</span><span class="sxs-lookup"><span data-stu-id="91273-116">-Location</span></span>
<span data-ttu-id="91273-117">Расположение для созданного ConnectedMachine.</span><span class="sxs-lookup"><span data-stu-id="91273-117">The location for the created ConnectedMachine.</span></span>

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

### <span data-ttu-id="91273-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="91273-118">-Name</span></span>
<span data-ttu-id="91273-119">Имя, которое будет использоваться для этого компьютера.</span><span class="sxs-lookup"><span data-stu-id="91273-119">The name that will be used for this machine.</span></span>
<span data-ttu-id="91273-120">Имя узла используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="91273-120">The hostname is used by default.</span></span>

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

### <span data-ttu-id="91273-121">-Прокси</span><span class="sxs-lookup"><span data-stu-id="91273-121">-Proxy</span></span>
<span data-ttu-id="91273-122">URI для прокси-сервера, который нужно использовать.</span><span class="sxs-lookup"><span data-stu-id="91273-122">The URI for the proxy server to use</span></span>

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

### <span data-ttu-id="91273-123">-PSSession</span><span class="sxs-lookup"><span data-stu-id="91273-123">-PSSession</span></span>
<span data-ttu-id="91273-124">Если указан, команда, на которой на Azure выводятся компьютеры, будет выполняться в каждом сеансе PSSession.</span><span class="sxs-lookup"><span data-stu-id="91273-124">When specified, the command that onboards machines to Azure will be run within each PSSession.</span></span>
<span data-ttu-id="91273-125">Примечание. Эта возможность работает только в Windows.</span><span class="sxs-lookup"><span data-stu-id="91273-125">NOTE: This only works on Windows for now.</span></span>

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

### <span data-ttu-id="91273-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91273-126">-ResourceGroupName</span></span>
<span data-ttu-id="91273-127">Имя группы ресурсов, в которую вы хотите добавить компьютер.</span><span class="sxs-lookup"><span data-stu-id="91273-127">The name of the resource group you want to add the machine to.</span></span>

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

### <span data-ttu-id="91273-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="91273-128">-SubscriptionId</span></span>
<span data-ttu-id="91273-129">Идентификатор подписки, в которую вы хотите добавить компьютер.</span><span class="sxs-lookup"><span data-stu-id="91273-129">The ID of the subscription you want to add the machine to.</span></span>

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

### <span data-ttu-id="91273-130">-Тег</span><span class="sxs-lookup"><span data-stu-id="91273-130">-Tag</span></span>
<span data-ttu-id="91273-131">Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="91273-131">Resource tags.</span></span>

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

### <span data-ttu-id="91273-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91273-132">CommonParameters</span></span>
<span data-ttu-id="91273-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="91273-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91273-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="91273-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91273-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="91273-135">INPUTS</span></span>

## <span data-ttu-id="91273-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="91273-136">OUTPUTS</span></span>

## <span data-ttu-id="91273-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="91273-137">NOTES</span></span>

<span data-ttu-id="91273-138">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="91273-138">ALIASES</span></span>

## <span data-ttu-id="91273-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="91273-139">RELATED LINKS</span></span>

