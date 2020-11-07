---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubKey.md
ms.openlocfilehash: 8be39cb4b4b173d3b87efbf0b7ecea72ae233061
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733056"
---
# <span data-ttu-id="4820c-101">New-AzureRmEventHubKey</span><span class="sxs-lookup"><span data-stu-id="4820c-101">New-AzureRmEventHubKey</span></span>

## <span data-ttu-id="4820c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4820c-102">SYNOPSIS</span></span>
<span data-ttu-id="4820c-103">Создает новый первичный или вторичный ключ для указанного правила авторизации концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="4820c-103">Creates a new primary or secondary key for the specified Event Hubs authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4820c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4820c-104">SYNTAX</span></span>

### <span data-ttu-id="4820c-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4820c-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-RegenerateKey] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4820c-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="4820c-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-RegenerateKey] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4820c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4820c-107">DESCRIPTION</span></span>
<span data-ttu-id="4820c-108">Командлет New-AzureRmEventHubKey повторно создает первичный или дополнительный ключ SAS для указанного правила авторизации концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="4820c-108">The New-AzureRmEventHubKey cmdlet regenerates the primary or secondary SAS key for the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="4820c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4820c-109">EXAMPLES</span></span>

### <span data-ttu-id="4820c-110">Пример 1,1</span><span class="sxs-lookup"><span data-stu-id="4820c-110">Example 1.1</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="4820c-111">Повторно создает первичный ключ для правила авторизации \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="4820c-111">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="4820c-112">Пример 1,2</span><span class="sxs-lookup"><span data-stu-id="4820c-112">Example 1.2</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="4820c-113">Повторно создает первичный ключ для правила авторизации \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="4820c-113">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="4820c-114">Пример 2,1</span><span class="sxs-lookup"><span data-stu-id="4820c-114">Example 2.1</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

### <span data-ttu-id="4820c-115">Пример 2,2</span><span class="sxs-lookup"><span data-stu-id="4820c-115">Example 2.2</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

<span data-ttu-id="4820c-116">Повторно создает вторичный ключ для правила авторизации \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="4820c-116">Regenerates the secondary key for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="4820c-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4820c-117">PARAMETERS</span></span>

### <span data-ttu-id="4820c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4820c-118">-DefaultProfile</span></span>
<span data-ttu-id="4820c-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4820c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4820c-120">-EventHub</span><span class="sxs-lookup"><span data-stu-id="4820c-120">-EventHub</span></span>
<span data-ttu-id="4820c-121">Имя EventHub</span><span class="sxs-lookup"><span data-stu-id="4820c-121">EventHub Name</span></span>

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4820c-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4820c-122">-Name</span></span>
<span data-ttu-id="4820c-123">Имя AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="4820c-123">AuthorizationRule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4820c-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4820c-124">-Namespace</span></span>
<span data-ttu-id="4820c-125">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="4820c-125">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4820c-126">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="4820c-126">-RegenerateKey</span></span>
<span data-ttu-id="4820c-127">Повторное создание ключей-"PrimaryKey"/"SecondaryKey"</span><span class="sxs-lookup"><span data-stu-id="4820c-127">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4820c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4820c-128">-ResourceGroupName</span></span>
<span data-ttu-id="4820c-129">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="4820c-129">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4820c-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4820c-130">-Confirm</span></span>
<span data-ttu-id="4820c-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4820c-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4820c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4820c-132">-WhatIf</span></span>
<span data-ttu-id="4820c-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4820c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4820c-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4820c-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4820c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4820c-135">CommonParameters</span></span>
<span data-ttu-id="4820c-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4820c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="4820c-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4820c-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4820c-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4820c-138">INPUTS</span></span>

### <span data-ttu-id="4820c-139">System. String</span><span class="sxs-lookup"><span data-stu-id="4820c-139">System.String</span></span>


## <span data-ttu-id="4820c-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4820c-140">OUTPUTS</span></span>

### <span data-ttu-id="4820c-141">Microsoft. Azure. Commands. EventHub. Models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="4820c-141">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>


## <span data-ttu-id="4820c-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="4820c-142">NOTES</span></span>

## <span data-ttu-id="4820c-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4820c-143">RELATED LINKS</span></span>
