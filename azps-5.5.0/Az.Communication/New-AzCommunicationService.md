---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/new-azcommunicationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/New-AzCommunicationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/New-AzCommunicationService.md
ms.openlocfilehash: 821590b158478c38e5d4e997254e98a802d4befd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100233449"
---
# <span data-ttu-id="cd506-101">New-AzCommunicationService</span><span class="sxs-lookup"><span data-stu-id="cd506-101">New-AzCommunicationService</span></span>

## <span data-ttu-id="cd506-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd506-102">SYNOPSIS</span></span>
<span data-ttu-id="cd506-103">Создайте новую службу communicationService или обновите существующую.</span><span class="sxs-lookup"><span data-stu-id="cd506-103">Create a new CommunicationService or update an existing CommunicationService.</span></span>

## <span data-ttu-id="cd506-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cd506-104">SYNTAX</span></span>

```
New-AzCommunicationService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DataLocation <String>] [-Location <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cd506-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd506-105">DESCRIPTION</span></span>
<span data-ttu-id="cd506-106">Создайте новую службу communicationService или обновите существующую.</span><span class="sxs-lookup"><span data-stu-id="cd506-106">Create a new CommunicationService or update an existing CommunicationService.</span></span>

## <span data-ttu-id="cd506-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cd506-107">EXAMPLES</span></span>

### <span data-ttu-id="cd506-108">Пример 1. Создание ресурса ACS</span><span class="sxs-lookup"><span data-stu-id="cd506-108">Example 1: Create a ACS resource</span></span>
```powershell
PS C:\> New-AzCommunicationService -ResourceGroupName ContosoResourceProvider1 -Name ContosoAcsResource1 -DataLocation UnitedStates -Location Global

Location Name           Type                                          AzureAsyncOperation
-------- ----           ----                                          -------------------
Global   ContosoAcsResource1 Microsoft.Communication/communicationServices
```

<span data-ttu-id="cd506-109">Создание ресурса ACS с использованием указанных параметров.</span><span class="sxs-lookup"><span data-stu-id="cd506-109">Creates a ACS resource using the specified parameters.</span></span>

## <span data-ttu-id="cd506-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd506-110">PARAMETERS</span></span>

### <span data-ttu-id="cd506-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd506-111">-AsJob</span></span>
<span data-ttu-id="cd506-112">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="cd506-112">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd506-113">-DataLocation</span><span class="sxs-lookup"><span data-stu-id="cd506-113">-DataLocation</span></span>
<span data-ttu-id="cd506-114">Расположение, в котором служба связи хранит неавтные данные.</span><span class="sxs-lookup"><span data-stu-id="cd506-114">The location where the communication service stores its data at rest.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd506-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd506-115">-DefaultProfile</span></span>
<span data-ttu-id="cd506-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cd506-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd506-117">-Location</span><span class="sxs-lookup"><span data-stu-id="cd506-117">-Location</span></span>
<span data-ttu-id="cd506-118">Расположение Azure, в котором запущена служба CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="cd506-118">The Azure location where the CommunicationService is running.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd506-119">-Name</span><span class="sxs-lookup"><span data-stu-id="cd506-119">-Name</span></span>
<span data-ttu-id="cd506-120">Имя ресурса CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="cd506-120">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CommunicationServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd506-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="cd506-121">-NoWait</span></span>
<span data-ttu-id="cd506-122">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="cd506-122">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd506-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd506-123">-ResourceGroupName</span></span>
<span data-ttu-id="cd506-124">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="cd506-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="cd506-125">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="cd506-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd506-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cd506-126">-SubscriptionId</span></span>
<span data-ttu-id="cd506-127">Возвращает идентификатор подписки, который однозначно определяет подписку на Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cd506-127">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="cd506-128">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="cd506-128">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd506-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="cd506-129">-Tag</span></span>
<span data-ttu-id="cd506-130">Теги службы, которые являются списком пар ключевых значений, которые описывают ресурс.</span><span class="sxs-lookup"><span data-stu-id="cd506-130">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd506-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cd506-131">-Confirm</span></span>
<span data-ttu-id="cd506-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="cd506-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd506-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd506-133">-WhatIf</span></span>
<span data-ttu-id="cd506-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd506-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd506-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="cd506-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd506-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd506-136">CommonParameters</span></span>
<span data-ttu-id="cd506-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd506-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd506-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cd506-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd506-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cd506-139">INPUTS</span></span>

## <span data-ttu-id="cd506-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cd506-140">OUTPUTS</span></span>

### <span data-ttu-id="cd506-141">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span><span class="sxs-lookup"><span data-stu-id="cd506-141">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span></span>

## <span data-ttu-id="cd506-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cd506-142">NOTES</span></span>

<span data-ttu-id="cd506-143">ALIASES</span><span class="sxs-lookup"><span data-stu-id="cd506-143">ALIASES</span></span>

## <span data-ttu-id="cd506-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cd506-144">RELATED LINKS</span></span>

