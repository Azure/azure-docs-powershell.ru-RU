---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubauthorizationrulesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRuleSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRuleSASToken.md
ms.openlocfilehash: 24348c44ef9b529507c50a689f181739d1474e22
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066632"
---
# <span data-ttu-id="2c9a8-101">New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="2c9a8-101">New-AzEventHubAuthorizationRuleSASToken</span></span>

## <span data-ttu-id="2c9a8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2c9a8-102">SYNOPSIS</span></span>
<span data-ttu-id="2c9a8-103">Создает маркер SAS для правила авторизации eventhub Azure для пространства имен/eventhub.</span><span class="sxs-lookup"><span data-stu-id="2c9a8-103">Generates a SAS token for Azure eventhub authorization rule of namespace/eventhub.</span></span> 

## <span data-ttu-id="2c9a8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2c9a8-104">SYNTAX</span></span>

```
New-AzEventHubAuthorizationRuleSASToken [-AuthorizationRuleId] <String> [-KeyType] <String>
 [-ExpiryTime] <DateTime> [-StartTime <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c9a8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c9a8-105">DESCRIPTION</span></span>
<span data-ttu-id="2c9a8-106">Командлет New-AzEventHubAuthorizationRuleSASToken создает маркер подписи общего доступа (SAS) для Azure Eventhub Namesapce или Azure Eventhub.</span><span class="sxs-lookup"><span data-stu-id="2c9a8-106">The New-AzEventHubAuthorizationRuleSASToken cmdlet generates a Shared Access Signature (SAS) token for an Azure Eventhub Namesapce or Azure Eventhub</span></span>

## <span data-ttu-id="2c9a8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2c9a8-107">EXAMPLES</span></span>

### <span data-ttu-id="2c9a8-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2c9a8-108">Example 1</span></span>
```powershell
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> $SasToken = New-AzEventHubAuthorizationRuleSASToken -AuthorizationRuleId $updatedAuthRule.Id  -KeyType Primary -ExpiryTime $EndTime -StartTime $StartTime
```

<span data-ttu-id="2c9a8-109">Создание маркера SAS для заданного правила authorixation для пространства имен с временем начала и окончания.</span><span class="sxs-lookup"><span data-stu-id="2c9a8-109">Generate SAS token for the given authorixation rule for Namespace with start and expiry time..</span></span>

### <span data-ttu-id="2c9a8-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="2c9a8-110">Example 2</span></span>
```powershell
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> $SasToken = New-AzEventHubAuthorizationRuleSASToken -AuthorizationRuleId $updatedAuthRule.Id  -KeyType Primary -ExpiryTime $EndTime
```

<span data-ttu-id="2c9a8-111">Создание маркера SAS для заданного правила authorixation для пространства имен с истекшим сроком действия.</span><span class="sxs-lookup"><span data-stu-id="2c9a8-111">Generate SAS token for the given authorixation rule for Namespace with expiry time.</span></span>

## <span data-ttu-id="2c9a8-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2c9a8-112">PARAMETERS</span></span>

### <span data-ttu-id="2c9a8-113">-AuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="2c9a8-113">-AuthorizationRuleId</span></span>
<span data-ttu-id="2c9a8-114">ResourceId (ИД) правила Authoraization</span><span class="sxs-lookup"><span data-stu-id="2c9a8-114">ARM ResourceId of the Authoraization Rule</span></span>

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

### <span data-ttu-id="2c9a8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c9a8-115">-DefaultProfile</span></span>
<span data-ttu-id="2c9a8-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2c9a8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c9a8-117">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="2c9a8-117">-ExpiryTime</span></span>
<span data-ttu-id="2c9a8-118">Время окончания срока действия</span><span class="sxs-lookup"><span data-stu-id="2c9a8-118">Expiry Time</span></span>

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

### <span data-ttu-id="2c9a8-119">-KeyType</span><span class="sxs-lookup"><span data-stu-id="2c9a8-119">-KeyType</span></span>
<span data-ttu-id="2c9a8-120">Тип ключа</span><span class="sxs-lookup"><span data-stu-id="2c9a8-120">Key Type</span></span>

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

### <span data-ttu-id="2c9a8-121">-StartTime</span><span class="sxs-lookup"><span data-stu-id="2c9a8-121">-StartTime</span></span>
<span data-ttu-id="2c9a8-122">Время начала</span><span class="sxs-lookup"><span data-stu-id="2c9a8-122">Start Time</span></span>

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

### <span data-ttu-id="2c9a8-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2c9a8-123">-Confirm</span></span>
<span data-ttu-id="2c9a8-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2c9a8-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c9a8-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c9a8-125">-WhatIf</span></span>
<span data-ttu-id="2c9a8-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2c9a8-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c9a8-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2c9a8-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c9a8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c9a8-128">CommonParameters</span></span>
<span data-ttu-id="2c9a8-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2c9a8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="2c9a8-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c9a8-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c9a8-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2c9a8-131">INPUTS</span></span>

### <span data-ttu-id="2c9a8-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2c9a8-132">System.String</span></span>

### <span data-ttu-id="2c9a8-133">System. Nullable "1 [[System. DateTime, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="2c9a8-133">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="2c9a8-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c9a8-134">OUTPUTS</span></span>

### <span data-ttu-id="2c9a8-135">Microsoft. Azure. Commands. EventHub. Models. PSSharedAccessSignatureAttributes</span><span class="sxs-lookup"><span data-stu-id="2c9a8-135">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessSignatureAttributes</span></span>

## <span data-ttu-id="2c9a8-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="2c9a8-136">NOTES</span></span>

## <span data-ttu-id="2c9a8-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2c9a8-137">RELATED LINKS</span></span>
