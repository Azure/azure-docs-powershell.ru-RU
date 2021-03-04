---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/new-azeventhubauthorizationrulesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRuleSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRuleSASToken.md
ms.openlocfilehash: 30a25f5101229076bad1219356edde5780364528
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957139"
---
# <span data-ttu-id="db2a9-101">New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="db2a9-101">New-AzEventHubAuthorizationRuleSASToken</span></span>

## <span data-ttu-id="db2a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db2a9-102">SYNOPSIS</span></span>
<span data-ttu-id="db2a9-103">Создает маркер SAS для правила авторизации Azure eventhub в области имен или е eventhub.</span><span class="sxs-lookup"><span data-stu-id="db2a9-103">Generates a SAS token for Azure eventhub authorization rule of namespace/eventhub.</span></span> 

## <span data-ttu-id="db2a9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="db2a9-104">SYNTAX</span></span>

```
New-AzEventHubAuthorizationRuleSASToken [-AuthorizationRuleId] <String> [-KeyType] <String>
 [-ExpiryTime] <DateTime> [-StartTime <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db2a9-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="db2a9-105">DESCRIPTION</span></span>
<span data-ttu-id="db2a9-106">Для New-AzEventHubAuthorizationRuleSASToken Azure Eventhub или Azure Eventhub создается маркер подписи общего доступа (SAS).</span><span class="sxs-lookup"><span data-stu-id="db2a9-106">The New-AzEventHubAuthorizationRuleSASToken cmdlet generates a Shared Access Signature (SAS) token for an Azure Eventhub Namesapce or Azure Eventhub</span></span>

## <span data-ttu-id="db2a9-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="db2a9-107">EXAMPLES</span></span>

### <span data-ttu-id="db2a9-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="db2a9-108">Example 1</span></span>
```powershell
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> $SasToken = New-AzEventHubAuthorizationRuleSASToken -AuthorizationRuleId $updatedAuthRule.Id  -KeyType Primary -ExpiryTime $EndTime -StartTime $StartTime
```

<span data-ttu-id="db2a9-109">Создание маркера SAS для заданного правила авторизации для пространства имен со сроком начала и окончания срока действия.</span><span class="sxs-lookup"><span data-stu-id="db2a9-109">Generate SAS token for the given authorixation rule for Namespace with start and expiry time..</span></span>

### <span data-ttu-id="db2a9-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="db2a9-110">Example 2</span></span>
```powershell
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> $SasToken = New-AzEventHubAuthorizationRuleSASToken -AuthorizationRuleId $updatedAuthRule.Id  -KeyType Primary -ExpiryTime $EndTime
```

<span data-ttu-id="db2a9-111">Создание маркера SAS для заданного правила авторизации для пространства имен со сроком действия.</span><span class="sxs-lookup"><span data-stu-id="db2a9-111">Generate SAS token for the given authorixation rule for Namespace with expiry time.</span></span>

## <span data-ttu-id="db2a9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db2a9-112">PARAMETERS</span></span>

### <span data-ttu-id="db2a9-113">-AuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="db2a9-113">-AuthorizationRuleId</span></span>
<span data-ttu-id="db2a9-114">ARM ResourceId правила авторизации</span><span class="sxs-lookup"><span data-stu-id="db2a9-114">ARM ResourceId of the Authoraization Rule</span></span>

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

### <span data-ttu-id="db2a9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db2a9-115">-DefaultProfile</span></span>
<span data-ttu-id="db2a9-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="db2a9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db2a9-117">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="db2a9-117">-ExpiryTime</span></span>
<span data-ttu-id="db2a9-118">Срок действия истекает</span><span class="sxs-lookup"><span data-stu-id="db2a9-118">Expiry Time</span></span>

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

### <span data-ttu-id="db2a9-119">-KeyType</span><span class="sxs-lookup"><span data-stu-id="db2a9-119">-KeyType</span></span>
<span data-ttu-id="db2a9-120">Тип ключа</span><span class="sxs-lookup"><span data-stu-id="db2a9-120">Key Type</span></span>

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

### <span data-ttu-id="db2a9-121">-StartTime</span><span class="sxs-lookup"><span data-stu-id="db2a9-121">-StartTime</span></span>
<span data-ttu-id="db2a9-122">Время начала</span><span class="sxs-lookup"><span data-stu-id="db2a9-122">Start Time</span></span>

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

### <span data-ttu-id="db2a9-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="db2a9-123">-Confirm</span></span>
<span data-ttu-id="db2a9-124">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="db2a9-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db2a9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db2a9-125">-WhatIf</span></span>
<span data-ttu-id="db2a9-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db2a9-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db2a9-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="db2a9-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db2a9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db2a9-128">CommonParameters</span></span>
<span data-ttu-id="db2a9-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db2a9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="db2a9-130">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db2a9-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db2a9-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="db2a9-131">INPUTS</span></span>

### <span data-ttu-id="db2a9-132">System.String</span><span class="sxs-lookup"><span data-stu-id="db2a9-132">System.String</span></span>

### <span data-ttu-id="db2a9-133">System.Nullable'1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="db2a9-133">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="db2a9-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="db2a9-134">OUTPUTS</span></span>

### <span data-ttu-id="db2a9-135">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessSignatureAttributes</span><span class="sxs-lookup"><span data-stu-id="db2a9-135">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessSignatureAttributes</span></span>

## <span data-ttu-id="db2a9-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="db2a9-136">NOTES</span></span>

## <span data-ttu-id="db2a9-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="db2a9-137">RELATED LINKS</span></span>
