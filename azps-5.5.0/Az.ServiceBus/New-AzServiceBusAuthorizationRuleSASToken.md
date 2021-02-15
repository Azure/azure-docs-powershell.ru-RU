---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusauthorizationrulesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRuleSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRuleSASToken.md
ms.openlocfilehash: d314deb2515907b7d2b668d18d165a7fb0691509
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242213"
---
# <span data-ttu-id="95bc4-101">New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="95bc4-101">New-AzServiceBusAuthorizationRuleSASToken</span></span>

## <span data-ttu-id="95bc4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95bc4-102">SYNOPSIS</span></span>
<span data-ttu-id="95bc4-103">Создает tolen SAS для правила авторизации службы Azure в области имен, очереди или теме.</span><span class="sxs-lookup"><span data-stu-id="95bc4-103">Generates a SAS tolen for Azure servicebus authorization rule of namespace/queue/topic.</span></span> 

## <span data-ttu-id="95bc4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="95bc4-104">SYNTAX</span></span>

```
New-AzServiceBusAuthorizationRuleSASToken [-AuthorizationRuleId] <String> [-KeyType] <String>
 [-ExpiryTime] <DateTime> [-StartTime <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95bc4-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="95bc4-105">DESCRIPTION</span></span>
<span data-ttu-id="95bc4-106">Для New-AzServiceBusAuthorizationRuleSASToken Azure Eventhub или Azure Eventhub создается маркер подписи общего доступа (SAS).</span><span class="sxs-lookup"><span data-stu-id="95bc4-106">The New-AzServiceBusAuthorizationRuleSASToken cmdlet generates a Shared Access Signature (SAS) token for an Azure Eventhub Namesapce or Azure Eventhub</span></span>

## <span data-ttu-id="95bc4-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="95bc4-107">EXAMPLES</span></span>

### <span data-ttu-id="95bc4-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="95bc4-108">Example 1</span></span>
```powershell
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> $SasToken = New-AzServiceBusAuthorizationRuleSASToken -AuthorizationRuleId $updatedAuthRule.Id  -KeyType Primary -ExpiryTime $EndTime -StartTime $StartTime
```

<span data-ttu-id="95bc4-109">Создание маркера SAS для заданного правила авторизации для пространства имен со сроком начала и окончания срока действия.</span><span class="sxs-lookup"><span data-stu-id="95bc4-109">Generate SAS token for the given authorixation rule for Namespace with start and expiry time..</span></span>

### <span data-ttu-id="95bc4-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="95bc4-110">Example 2</span></span>
```powershell
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> $SasToken = New-AzServiceBusAuthorizationRuleSASToken -AuthorizationRuleId $updatedAuthRule.Id  -KeyType Primary -ExpiryTime $EndTime
```

<span data-ttu-id="95bc4-111">Создание маркера SAS для заданного правила авторизации для пространства имен со сроком действия.</span><span class="sxs-lookup"><span data-stu-id="95bc4-111">Generate SAS token for the given authorixation rule for Namespace with expiry time.</span></span>

## <span data-ttu-id="95bc4-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="95bc4-112">PARAMETERS</span></span>

### <span data-ttu-id="95bc4-113">-AuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="95bc4-113">-AuthorizationRuleId</span></span>
<span data-ttu-id="95bc4-114">ARM ResourceId правила авторизации</span><span class="sxs-lookup"><span data-stu-id="95bc4-114">ARM ResourceId of the Authoraization Rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95bc4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95bc4-115">-DefaultProfile</span></span>
<span data-ttu-id="95bc4-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="95bc4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95bc4-117">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="95bc4-117">-ExpiryTime</span></span>
<span data-ttu-id="95bc4-118">Срок действия истекает</span><span class="sxs-lookup"><span data-stu-id="95bc4-118">Expiry Time</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95bc4-119">-KeyType</span><span class="sxs-lookup"><span data-stu-id="95bc4-119">-KeyType</span></span>
<span data-ttu-id="95bc4-120">Тип ключа</span><span class="sxs-lookup"><span data-stu-id="95bc4-120">Key Type</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95bc4-121">-StartTime</span><span class="sxs-lookup"><span data-stu-id="95bc4-121">-StartTime</span></span>
<span data-ttu-id="95bc4-122">Время начала</span><span class="sxs-lookup"><span data-stu-id="95bc4-122">Start Time</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95bc4-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="95bc4-123">-Confirm</span></span>
<span data-ttu-id="95bc4-124">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95bc4-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95bc4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95bc4-125">-WhatIf</span></span>
<span data-ttu-id="95bc4-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95bc4-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95bc4-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="95bc4-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95bc4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95bc4-128">CommonParameters</span></span>
<span data-ttu-id="95bc4-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95bc4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="95bc4-130">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95bc4-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95bc4-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="95bc4-131">INPUTS</span></span>

### <span data-ttu-id="95bc4-132">System.String</span><span class="sxs-lookup"><span data-stu-id="95bc4-132">System.String</span></span>

### <span data-ttu-id="95bc4-133">System.Nullable'1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="95bc4-133">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="95bc4-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="95bc4-134">OUTPUTS</span></span>

### <span data-ttu-id="95bc4-135">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessSignatureAttributes</span><span class="sxs-lookup"><span data-stu-id="95bc4-135">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessSignatureAttributes</span></span>

## <span data-ttu-id="95bc4-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="95bc4-136">NOTES</span></span>

## <span data-ttu-id="95bc4-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="95bc4-137">RELATED LINKS</span></span>