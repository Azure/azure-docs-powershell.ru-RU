---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusauthorizationrulesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRuleSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRuleSASToken.md
ms.openlocfilehash: d314deb2515907b7d2b668d18d165a7fb0691509
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249460"
---
# <span data-ttu-id="c7e12-101">New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="c7e12-101">New-AzServiceBusAuthorizationRuleSASToken</span></span>

## <span data-ttu-id="c7e12-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c7e12-102">SYNOPSIS</span></span>
<span data-ttu-id="c7e12-103">Создание правила авторизации tolen для Azure servicebus для пространства имен/очереди/темы.</span><span class="sxs-lookup"><span data-stu-id="c7e12-103">Generates a SAS tolen for Azure servicebus authorization rule of namespace/queue/topic.</span></span> 

## <span data-ttu-id="c7e12-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c7e12-104">SYNTAX</span></span>

```
New-AzServiceBusAuthorizationRuleSASToken [-AuthorizationRuleId] <String> [-KeyType] <String>
 [-ExpiryTime] <DateTime> [-StartTime <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7e12-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c7e12-105">DESCRIPTION</span></span>
<span data-ttu-id="c7e12-106">Командлет New-AzServiceBusAuthorizationRuleSASToken создает маркер подписи общего доступа (SAS) для Azure Eventhub Namesapce или Azure Eventhub.</span><span class="sxs-lookup"><span data-stu-id="c7e12-106">The New-AzServiceBusAuthorizationRuleSASToken cmdlet generates a Shared Access Signature (SAS) token for an Azure Eventhub Namesapce or Azure Eventhub</span></span>

## <span data-ttu-id="c7e12-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c7e12-107">EXAMPLES</span></span>

### <span data-ttu-id="c7e12-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c7e12-108">Example 1</span></span>
```powershell
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> $SasToken = New-AzServiceBusAuthorizationRuleSASToken -AuthorizationRuleId $updatedAuthRule.Id  -KeyType Primary -ExpiryTime $EndTime -StartTime $StartTime
```

<span data-ttu-id="c7e12-109">Создание маркера SAS для заданного правила authorixation для пространства имен с временем начала и окончания.</span><span class="sxs-lookup"><span data-stu-id="c7e12-109">Generate SAS token for the given authorixation rule for Namespace with start and expiry time..</span></span>

### <span data-ttu-id="c7e12-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c7e12-110">Example 2</span></span>
```powershell
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> $SasToken = New-AzServiceBusAuthorizationRuleSASToken -AuthorizationRuleId $updatedAuthRule.Id  -KeyType Primary -ExpiryTime $EndTime
```

<span data-ttu-id="c7e12-111">Создание маркера SAS для заданного правила authorixation для пространства имен с истекшим сроком действия.</span><span class="sxs-lookup"><span data-stu-id="c7e12-111">Generate SAS token for the given authorixation rule for Namespace with expiry time.</span></span>

## <span data-ttu-id="c7e12-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c7e12-112">PARAMETERS</span></span>

### <span data-ttu-id="c7e12-113">-AuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="c7e12-113">-AuthorizationRuleId</span></span>
<span data-ttu-id="c7e12-114">ResourceId (ИД) правила Authoraization</span><span class="sxs-lookup"><span data-stu-id="c7e12-114">ARM ResourceId of the Authoraization Rule</span></span>

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

### <span data-ttu-id="c7e12-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7e12-115">-DefaultProfile</span></span>
<span data-ttu-id="c7e12-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c7e12-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7e12-117">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="c7e12-117">-ExpiryTime</span></span>
<span data-ttu-id="c7e12-118">Время окончания срока действия</span><span class="sxs-lookup"><span data-stu-id="c7e12-118">Expiry Time</span></span>

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

### <span data-ttu-id="c7e12-119">-KeyType</span><span class="sxs-lookup"><span data-stu-id="c7e12-119">-KeyType</span></span>
<span data-ttu-id="c7e12-120">Тип ключа</span><span class="sxs-lookup"><span data-stu-id="c7e12-120">Key Type</span></span>

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

### <span data-ttu-id="c7e12-121">-StartTime</span><span class="sxs-lookup"><span data-stu-id="c7e12-121">-StartTime</span></span>
<span data-ttu-id="c7e12-122">Время начала</span><span class="sxs-lookup"><span data-stu-id="c7e12-122">Start Time</span></span>

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

### <span data-ttu-id="c7e12-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c7e12-123">-Confirm</span></span>
<span data-ttu-id="c7e12-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c7e12-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7e12-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7e12-125">-WhatIf</span></span>
<span data-ttu-id="c7e12-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c7e12-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7e12-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c7e12-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7e12-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7e12-128">CommonParameters</span></span>
<span data-ttu-id="c7e12-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c7e12-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c7e12-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7e12-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7e12-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c7e12-131">INPUTS</span></span>

### <span data-ttu-id="c7e12-132">System. String</span><span class="sxs-lookup"><span data-stu-id="c7e12-132">System.String</span></span>

### <span data-ttu-id="c7e12-133">System. Nullable "1 [[System. DateTime, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="c7e12-133">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="c7e12-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c7e12-134">OUTPUTS</span></span>

### <span data-ttu-id="c7e12-135">Microsoft. Azure. Commands. ServiceBus. Models. PSSharedAccessSignatureAttributes</span><span class="sxs-lookup"><span data-stu-id="c7e12-135">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessSignatureAttributes</span></span>

## <span data-ttu-id="c7e12-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="c7e12-136">NOTES</span></span>

## <span data-ttu-id="c7e12-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c7e12-137">RELATED LINKS</span></span>