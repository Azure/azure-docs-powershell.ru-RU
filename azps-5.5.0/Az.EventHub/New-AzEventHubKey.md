---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubKey.md
ms.openlocfilehash: 477884e676118f461578be500715fd3698957003
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100230393"
---
# <span data-ttu-id="cf945-101">New-AzEventHubKey</span><span class="sxs-lookup"><span data-stu-id="cf945-101">New-AzEventHubKey</span></span>

## <span data-ttu-id="cf945-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf945-102">SYNOPSIS</span></span>
<span data-ttu-id="cf945-103">Создает новый первичный или дополнительный ключ для заданного правила авторизации "Концентраторы событий".</span><span class="sxs-lookup"><span data-stu-id="cf945-103">Creates a new primary or secondary key for the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="cf945-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cf945-104">SYNTAX</span></span>

### <span data-ttu-id="cf945-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cf945-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-RegenerateKey] <String> [[-KeyValue] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf945-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="cf945-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String> [-Name] <String>
 [-RegenerateKey] <String> [[-KeyValue] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf945-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf945-107">DESCRIPTION</span></span>
<span data-ttu-id="cf945-108">Этот New-AzEventHubKey сгенерирует первичный или дополнительный ключ SAS для указанного правила авторизации На концентраторах событий.</span><span class="sxs-lookup"><span data-stu-id="cf945-108">The New-AzEventHubKey cmdlet regenerates the primary or secondary SAS key for the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="cf945-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cf945-109">EXAMPLES</span></span>

### <span data-ttu-id="cf945-110">Пример 1. Namespace — AuthorizationRule PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="cf945-110">Example 1: Namespace - AuthorizationRule PrimaryKey</span></span>
```powershell
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="cf945-111">Повторно сгенерирует первичный ключ для правила авторизации \` MyAuthRuleName. \`</span><span class="sxs-lookup"><span data-stu-id="cf945-111">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="cf945-112">Пример 2: EventHub — AuthorizationRule PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="cf945-112">Example 2: EventHub - AuthorizationRule PrimaryKey</span></span>
```powershell
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="cf945-113">Повторно сгенерирует первичный ключ для правила авторизации \` MyAuthRuleName. \`</span><span class="sxs-lookup"><span data-stu-id="cf945-113">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="cf945-114">Пример 3. - Namespace - AuthorizationRule SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="cf945-114">Example 3: - Namespace - AuthorizationRule SecondaryKey</span></span>
```powershell
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

### <span data-ttu-id="cf945-115">Пример 4. EventHub — AuthorizationRule SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="cf945-115">Example 4: EventHub - AuthorizationRule SecondaryKey</span></span>
```powershell
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

<span data-ttu-id="cf945-116">Повторно сгенерирует дополнительный ключ для правила авторизации \` MyAuthRuleName. \`</span><span class="sxs-lookup"><span data-stu-id="cf945-116">Regenerates the secondary key for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="cf945-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cf945-117">PARAMETERS</span></span>

### <span data-ttu-id="cf945-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf945-118">-DefaultProfile</span></span>
<span data-ttu-id="cf945-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cf945-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf945-120">-EventHub</span><span class="sxs-lookup"><span data-stu-id="cf945-120">-EventHub</span></span>
<span data-ttu-id="cf945-121">EventHub Name</span><span class="sxs-lookup"><span data-stu-id="cf945-121">EventHub Name</span></span>

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

### <span data-ttu-id="cf945-122">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="cf945-122">-KeyValue</span></span>
<span data-ttu-id="cf945-123">Ключ 256-битной кодировки base64 для подписания и проверки маркера SAS.</span><span class="sxs-lookup"><span data-stu-id="cf945-123">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

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

### <span data-ttu-id="cf945-124">-Name</span><span class="sxs-lookup"><span data-stu-id="cf945-124">-Name</span></span>
<span data-ttu-id="cf945-125">Имяrule authorizationRule</span><span class="sxs-lookup"><span data-stu-id="cf945-125">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="cf945-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="cf945-126">-Namespace</span></span>
<span data-ttu-id="cf945-127">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="cf945-127">Namespace Name</span></span>

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

### <span data-ttu-id="cf945-128">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="cf945-128">-RegenerateKey</span></span>
<span data-ttu-id="cf945-129">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'</span><span class="sxs-lookup"><span data-stu-id="cf945-129">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'</span></span>

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

### <span data-ttu-id="cf945-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf945-130">-ResourceGroupName</span></span>
<span data-ttu-id="cf945-131">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="cf945-131">Resource Group Name</span></span>

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

### <span data-ttu-id="cf945-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cf945-132">-Confirm</span></span>
<span data-ttu-id="cf945-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf945-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf945-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf945-134">-WhatIf</span></span>
<span data-ttu-id="cf945-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf945-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf945-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="cf945-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf945-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf945-137">CommonParameters</span></span>
<span data-ttu-id="cf945-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf945-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf945-139">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf945-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf945-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cf945-140">INPUTS</span></span>

### <span data-ttu-id="cf945-141">System.String</span><span class="sxs-lookup"><span data-stu-id="cf945-141">System.String</span></span>

## <span data-ttu-id="cf945-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cf945-142">OUTPUTS</span></span>

### <span data-ttu-id="cf945-143">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="cf945-143">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="cf945-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cf945-144">NOTES</span></span>

## <span data-ttu-id="cf945-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cf945-145">RELATED LINKS</span></span>
