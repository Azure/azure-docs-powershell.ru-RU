---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/New-AzEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/New-AzEventHubKey.md
ms.openlocfilehash: 50ec39882a510393e304efae4c7cbc9469d14d91
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910384"
---
# <span data-ttu-id="1dafd-101">New-AzEventHubKey</span><span class="sxs-lookup"><span data-stu-id="1dafd-101">New-AzEventHubKey</span></span>

## <span data-ttu-id="1dafd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1dafd-102">SYNOPSIS</span></span>
<span data-ttu-id="1dafd-103">Создает новый первичный или вторичный ключ для указанного правила авторизации концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="1dafd-103">Creates a new primary or secondary key for the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="1dafd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1dafd-104">SYNTAX</span></span>

### <span data-ttu-id="1dafd-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1dafd-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-RegenerateKey] <String> [[-KeyValue] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dafd-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="1dafd-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String> [-Name] <String>
 [-RegenerateKey] <String> [[-KeyValue] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1dafd-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1dafd-107">DESCRIPTION</span></span>
<span data-ttu-id="1dafd-108">Командлет New-AzEventHubKey повторно создает первичный или дополнительный ключ SAS для указанного правила авторизации концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="1dafd-108">The New-AzEventHubKey cmdlet regenerates the primary or secondary SAS key for the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="1dafd-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1dafd-109">EXAMPLES</span></span>

### <span data-ttu-id="1dafd-110">Пример 1,1-Namespace-AuthorizationRule PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="1dafd-110">Example 1.1 - Namespace - AuthorizationRule PrimaryKey</span></span>
```
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="1dafd-111">Повторно создает первичный ключ для правила авторизации \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="1dafd-111">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="1dafd-112">Пример 1,2-EventHub-AuthorizationRule PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="1dafd-112">Example 1.2 - EventHub - AuthorizationRule PrimaryKey</span></span>
```
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="1dafd-113">Повторно создает первичный ключ для правила авторизации \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="1dafd-113">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="1dafd-114">Пример 2,1-Namespace-AuthorizationRule SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="1dafd-114">Example 2.1  - Namespace - AuthorizationRule SecondaryKey</span></span>
```
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

### <span data-ttu-id="1dafd-115">Пример 2,2-EventHub-AuthorizationRule SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="1dafd-115">Example 2.2 - EventHub - AuthorizationRule SecondaryKey</span></span>
```
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

<span data-ttu-id="1dafd-116">Повторно создает вторичный ключ для правила авторизации \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="1dafd-116">Regenerates the secondary key for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="1dafd-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1dafd-117">PARAMETERS</span></span>

### <span data-ttu-id="1dafd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dafd-118">-DefaultProfile</span></span>
<span data-ttu-id="1dafd-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1dafd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1dafd-120">-EventHub</span><span class="sxs-lookup"><span data-stu-id="1dafd-120">-EventHub</span></span>
<span data-ttu-id="1dafd-121">Имя EventHub</span><span class="sxs-lookup"><span data-stu-id="1dafd-121">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dafd-122">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="1dafd-122">-KeyValue</span></span>
<span data-ttu-id="1dafd-123">256-разрядный ключ в формате Base64 для подписывания и проверки маркера SAS.</span><span class="sxs-lookup"><span data-stu-id="1dafd-123">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dafd-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1dafd-124">-Name</span></span>
<span data-ttu-id="1dafd-125">Имя AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1dafd-125">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dafd-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="1dafd-126">-Namespace</span></span>
<span data-ttu-id="1dafd-127">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="1dafd-127">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dafd-128">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="1dafd-128">-RegenerateKey</span></span>
<span data-ttu-id="1dafd-129">Повторное создание ключей-"PrimaryKey"/"SecondaryKey"</span><span class="sxs-lookup"><span data-stu-id="1dafd-129">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dafd-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dafd-130">-ResourceGroupName</span></span>
<span data-ttu-id="1dafd-131">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="1dafd-131">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dafd-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1dafd-132">-Confirm</span></span>
<span data-ttu-id="1dafd-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1dafd-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dafd-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dafd-134">-WhatIf</span></span>
<span data-ttu-id="1dafd-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1dafd-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1dafd-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1dafd-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dafd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dafd-137">CommonParameters</span></span>
<span data-ttu-id="1dafd-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1dafd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dafd-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dafd-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dafd-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1dafd-140">INPUTS</span></span>

### <span data-ttu-id="1dafd-141">System. String</span><span class="sxs-lookup"><span data-stu-id="1dafd-141">System.String</span></span>

## <span data-ttu-id="1dafd-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1dafd-142">OUTPUTS</span></span>

### <span data-ttu-id="1dafd-143">Microsoft. Azure. Commands. EventHub. Models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="1dafd-143">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="1dafd-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="1dafd-144">NOTES</span></span>

## <span data-ttu-id="1dafd-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1dafd-145">RELATED LINKS</span></span>
