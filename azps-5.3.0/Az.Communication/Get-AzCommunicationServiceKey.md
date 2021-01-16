---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/get-azcommunicationservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationServiceKey.md
ms.openlocfilehash: e4a16b69e5919684b40d5b9f7fd4e97465d3565e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509281"
---
# <span data-ttu-id="fe9ec-101">Get-AzCommunicationServiceKey</span><span class="sxs-lookup"><span data-stu-id="fe9ec-101">Get-AzCommunicationServiceKey</span></span>

## <span data-ttu-id="fe9ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe9ec-102">SYNOPSIS</span></span>
<span data-ttu-id="fe9ec-103">Получите ключи доступа ресурса CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="fe9ec-103">Get the access keys of the CommunicationService resource.</span></span>

## <span data-ttu-id="fe9ec-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fe9ec-104">SYNTAX</span></span>

```
Get-AzCommunicationServiceKey -CommunicationServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fe9ec-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe9ec-105">DESCRIPTION</span></span>
<span data-ttu-id="fe9ec-106">Получите ключи доступа ресурса CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="fe9ec-106">Get the access keys of the CommunicationService resource.</span></span>

## <span data-ttu-id="fe9ec-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fe9ec-107">EXAMPLES</span></span>

### <span data-ttu-id="fe9ec-108">Пример 1. Извлечение ключа для указанной службы информационного сообщений</span><span class="sxs-lookup"><span data-stu-id="fe9ec-108">Example 1: Fetch the Key for the specified Communcation service</span></span>
```powershell
PS C:\> Get-AzCommunicationServiceKey -CommunicationServiceName ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1

PrimaryConnectionString              PrimaryKey            SecondaryConnectionString               SecondaryKey
-----------------------              ----------            -----------------------                 ----------
endpoint=<example-primary-endpoint>  <example-primarykey>  endpoint=<example-secondary-endpoint>   <example-secondarykey>
```

<span data-ttu-id="fe9ec-109">Отображаются клавиши ConnectionString и Key для указанной службы communcation.</span><span class="sxs-lookup"><span data-stu-id="fe9ec-109">Displays the ConnectionString and Key for the specified Communcation service.</span></span>

## <span data-ttu-id="fe9ec-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe9ec-110">PARAMETERS</span></span>

### <span data-ttu-id="fe9ec-111">-CommunicationServiceName</span><span class="sxs-lookup"><span data-stu-id="fe9ec-111">-CommunicationServiceName</span></span>
<span data-ttu-id="fe9ec-112">Имя ресурса CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="fe9ec-112">The name of the CommunicationService resource.</span></span>

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

### <span data-ttu-id="fe9ec-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe9ec-113">-DefaultProfile</span></span>
<span data-ttu-id="fe9ec-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fe9ec-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe9ec-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe9ec-115">-ResourceGroupName</span></span>
<span data-ttu-id="fe9ec-116">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="fe9ec-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="fe9ec-117">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="fe9ec-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="fe9ec-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fe9ec-118">-SubscriptionId</span></span>
<span data-ttu-id="fe9ec-119">Возвращает идентификатор подписки, который однозначно определяет подписку на Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="fe9ec-119">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="fe9ec-120">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="fe9ec-120">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe9ec-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fe9ec-121">-Confirm</span></span>
<span data-ttu-id="fe9ec-122">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="fe9ec-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe9ec-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe9ec-123">-WhatIf</span></span>
<span data-ttu-id="fe9ec-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe9ec-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe9ec-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="fe9ec-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe9ec-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe9ec-126">CommonParameters</span></span>
<span data-ttu-id="fe9ec-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe9ec-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe9ec-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fe9ec-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe9ec-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fe9ec-129">INPUTS</span></span>

## <span data-ttu-id="fe9ec-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fe9ec-130">OUTPUTS</span></span>

### <span data-ttu-id="fe9ec-131">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceKeys</span><span class="sxs-lookup"><span data-stu-id="fe9ec-131">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceKeys</span></span>

## <span data-ttu-id="fe9ec-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fe9ec-132">NOTES</span></span>

<span data-ttu-id="fe9ec-133">ALIASES</span><span class="sxs-lookup"><span data-stu-id="fe9ec-133">ALIASES</span></span>

## <span data-ttu-id="fe9ec-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fe9ec-134">RELATED LINKS</span></span>

