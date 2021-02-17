---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubauthorizationrulesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRuleSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRuleSASToken.md
ms.openlocfilehash: 24348c44ef9b529507c50a689f181739d1474e22
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100228457"
---
# <span data-ttu-id="6561f-101">New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="6561f-101">New-AzEventHubAuthorizationRuleSASToken</span></span>

## <span data-ttu-id="6561f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6561f-102">SYNOPSIS</span></span>
<span data-ttu-id="6561f-103">Создает маркер SAS для правила авторизации Azure eventhub в области имен или е eventhub.</span><span class="sxs-lookup"><span data-stu-id="6561f-103">Generates a SAS token for Azure eventhub authorization rule of namespace/eventhub.</span></span> 

## <span data-ttu-id="6561f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6561f-104">SYNTAX</span></span>

```
New-AzEventHubAuthorizationRuleSASToken [-AuthorizationRuleId] <String> [-KeyType] <String>
 [-ExpiryTime] <DateTime> [-StartTime <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6561f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6561f-105">DESCRIPTION</span></span>
<span data-ttu-id="6561f-106">Для New-AzEventHubAuthorizationRuleSASToken Azure Eventhub или Azure Eventhub создается маркер подписи общего доступа (SAS).</span><span class="sxs-lookup"><span data-stu-id="6561f-106">The New-AzEventHubAuthorizationRuleSASToken cmdlet generates a Shared Access Signature (SAS) token for an Azure Eventhub Namesapce or Azure Eventhub</span></span>

## <span data-ttu-id="6561f-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6561f-107">EXAMPLES</span></span>

### <span data-ttu-id="6561f-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6561f-108">Example 1</span></span>
```powershell
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> $SasToken = New-AzEventHubAuthorizationRuleSASToken -AuthorizationRuleId $updatedAuthRule.Id  -KeyType Primary -ExpiryTime $EndTime -StartTime $StartTime
```

<span data-ttu-id="6561f-109">Создание маркера SAS для заданного правила авторизации для пространства имен со сроком начала и окончания срока действия.</span><span class="sxs-lookup"><span data-stu-id="6561f-109">Generate SAS token for the given authorixation rule for Namespace with start and expiry time..</span></span>

### <span data-ttu-id="6561f-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6561f-110">Example 2</span></span>
```powershell
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> $SasToken = New-AzEventHubAuthorizationRuleSASToken -AuthorizationRuleId $updatedAuthRule.Id  -KeyType Primary -ExpiryTime $EndTime
```

<span data-ttu-id="6561f-111">Создание маркера SAS для заданного правила авторизации для пространства имен со сроком действия.</span><span class="sxs-lookup"><span data-stu-id="6561f-111">Generate SAS token for the given authorixation rule for Namespace with expiry time.</span></span>

## <span data-ttu-id="6561f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6561f-112">PARAMETERS</span></span>

### <span data-ttu-id="6561f-113">-AuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="6561f-113">-AuthorizationRuleId</span></span>
<span data-ttu-id="6561f-114">ARM ResourceId правила авторизации</span><span class="sxs-lookup"><span data-stu-id="6561f-114">ARM ResourceId of the Authoraization Rule</span></span>

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

### <span data-ttu-id="6561f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6561f-115">-DefaultProfile</span></span>
<span data-ttu-id="6561f-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6561f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6561f-117">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="6561f-117">-ExpiryTime</span></span>
<span data-ttu-id="6561f-118">Срок действия истекает</span><span class="sxs-lookup"><span data-stu-id="6561f-118">Expiry Time</span></span>

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

### <span data-ttu-id="6561f-119">-KeyType</span><span class="sxs-lookup"><span data-stu-id="6561f-119">-KeyType</span></span>
<span data-ttu-id="6561f-120">Тип ключа</span><span class="sxs-lookup"><span data-stu-id="6561f-120">Key Type</span></span>

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

### <span data-ttu-id="6561f-121">-StartTime</span><span class="sxs-lookup"><span data-stu-id="6561f-121">-StartTime</span></span>
<span data-ttu-id="6561f-122">Время начала</span><span class="sxs-lookup"><span data-stu-id="6561f-122">Start Time</span></span>

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

### <span data-ttu-id="6561f-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6561f-123">-Confirm</span></span>
<span data-ttu-id="6561f-124">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6561f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6561f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6561f-125">-WhatIf</span></span>
<span data-ttu-id="6561f-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6561f-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6561f-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6561f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6561f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6561f-128">CommonParameters</span></span>
<span data-ttu-id="6561f-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6561f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="6561f-130">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6561f-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6561f-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6561f-131">INPUTS</span></span>

### <span data-ttu-id="6561f-132">System.String</span><span class="sxs-lookup"><span data-stu-id="6561f-132">System.String</span></span>

### <span data-ttu-id="6561f-133">System.Nullable'1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="6561f-133">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="6561f-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6561f-134">OUTPUTS</span></span>

### <span data-ttu-id="6561f-135">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessSignatureAttributes</span><span class="sxs-lookup"><span data-stu-id="6561f-135">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessSignatureAttributes</span></span>

## <span data-ttu-id="6561f-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6561f-136">NOTES</span></span>

## <span data-ttu-id="6561f-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6561f-137">RELATED LINKS</span></span>
