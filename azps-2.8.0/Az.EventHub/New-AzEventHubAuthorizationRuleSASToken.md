---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubauthorizationrulesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRuleSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRuleSASToken.md
ms.openlocfilehash: a1064b42a5d30dde5ba51f3333ef1e4836ed7159
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720953"
---
# <span data-ttu-id="38522-101">New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="38522-101">New-AzEventHubAuthorizationRuleSASToken</span></span>

## <span data-ttu-id="38522-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="38522-102">SYNOPSIS</span></span>
<span data-ttu-id="38522-103">Создает tolen SAS для правила авторизации eventhub Azure для пространства имен/eventhub.</span><span class="sxs-lookup"><span data-stu-id="38522-103">Generates a SAS tolen for Azure eventhub authorization rule of namespace/eventhub.</span></span> 

## <span data-ttu-id="38522-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="38522-104">SYNTAX</span></span>

```
New-AzEventHubAuthorizationRuleSASToken [-AuthorizationRuleId] <String> [-KeyType] <String>
 [-ExpiryTime] <DateTime> [-StartTime <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38522-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="38522-105">DESCRIPTION</span></span>
<span data-ttu-id="38522-106">Командлет New-AzEventHubAuthorizationRuleSASToken создает маркер подписи общего доступа (SAS) для Azure Eventhub Namesapce или Azure Eventhub.</span><span class="sxs-lookup"><span data-stu-id="38522-106">The New-AzEventHubAuthorizationRuleSASToken cmdlet generates a Shared Access Signature (SAS) token for an Azure Eventhub Namesapce or Azure Eventhub</span></span>

## <span data-ttu-id="38522-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="38522-107">EXAMPLES</span></span>

### <span data-ttu-id="38522-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="38522-108">Example 1</span></span>
```powershell
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> $SasToken = New-AzEventHubAuthorizationRuleSASToken -AuthorizationRuleId $updatedAuthRule.Id  -KeyType Primary -ExpiryTime $EndTime -StartTime $StartTime
```

<span data-ttu-id="38522-109">Создание маркера SAS для заданного правила authorixation для пространства имен с временем начала и окончания.</span><span class="sxs-lookup"><span data-stu-id="38522-109">Generate SAS token for the given authorixation rule for Namespace with start and expiry time..</span></span>

### <span data-ttu-id="38522-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="38522-110">Example 2</span></span>
```powershell
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> $SasToken = New-AzEventHubAuthorizationRuleSASToken -AuthorizationRuleId $updatedAuthRule.Id  -KeyType Primary -ExpiryTime $EndTime
```

<span data-ttu-id="38522-111">Создание маркера SAS для заданного правила authorixation для пространства имен с истекшим сроком действия.</span><span class="sxs-lookup"><span data-stu-id="38522-111">Generate SAS token for the given authorixation rule for Namespace with expiry time.</span></span>

## <span data-ttu-id="38522-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="38522-112">PARAMETERS</span></span>

### <span data-ttu-id="38522-113">-AuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="38522-113">-AuthorizationRuleId</span></span>
<span data-ttu-id="38522-114">ResourceId (ИД) правила Authoraization</span><span class="sxs-lookup"><span data-stu-id="38522-114">ARM ResourceId of the Authoraization Rule</span></span>

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

### <span data-ttu-id="38522-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38522-115">-DefaultProfile</span></span>
<span data-ttu-id="38522-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="38522-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38522-117">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="38522-117">-ExpiryTime</span></span>
<span data-ttu-id="38522-118">Время окончания срока действия</span><span class="sxs-lookup"><span data-stu-id="38522-118">Expiry Time</span></span>

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

### <span data-ttu-id="38522-119">-KeyType</span><span class="sxs-lookup"><span data-stu-id="38522-119">-KeyType</span></span>
<span data-ttu-id="38522-120">Тип ключа</span><span class="sxs-lookup"><span data-stu-id="38522-120">Key Type</span></span>

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

### <span data-ttu-id="38522-121">-StartTime</span><span class="sxs-lookup"><span data-stu-id="38522-121">-StartTime</span></span>
<span data-ttu-id="38522-122">Время начала</span><span class="sxs-lookup"><span data-stu-id="38522-122">Start Time</span></span>

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

### <span data-ttu-id="38522-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="38522-123">-Confirm</span></span>
<span data-ttu-id="38522-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="38522-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38522-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38522-125">-WhatIf</span></span>
<span data-ttu-id="38522-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="38522-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38522-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="38522-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38522-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38522-128">CommonParameters</span></span>
<span data-ttu-id="38522-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="38522-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="38522-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38522-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38522-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="38522-131">INPUTS</span></span>

### <span data-ttu-id="38522-132">System. String</span><span class="sxs-lookup"><span data-stu-id="38522-132">System.String</span></span>

### <span data-ttu-id="38522-133">System. Nullable "1 [[System. DateTime, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="38522-133">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="38522-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="38522-134">OUTPUTS</span></span>

### <span data-ttu-id="38522-135">Microsoft. Azure. Commands. EventHub. Models. PSSharedAccessSignatureAttributes</span><span class="sxs-lookup"><span data-stu-id="38522-135">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessSignatureAttributes</span></span>

## <span data-ttu-id="38522-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="38522-136">NOTES</span></span>

## <span data-ttu-id="38522-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="38522-137">RELATED LINKS</span></span>
