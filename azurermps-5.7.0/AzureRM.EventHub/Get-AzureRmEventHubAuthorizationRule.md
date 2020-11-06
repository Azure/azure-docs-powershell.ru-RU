---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubAuthorizationRule.md
ms.openlocfilehash: 4d162122b82f592472fb31f1087db29faedf08cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567999"
---
# <span data-ttu-id="50802-101">Get-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="50802-101">Get-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="50802-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="50802-102">SYNOPSIS</span></span>
<span data-ttu-id="50802-103">Получает сведения о правиле авторизации или получает список правил авторизации.</span><span class="sxs-lookup"><span data-stu-id="50802-103">Gets the details of an authorization rule, or gets a list of authorization rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50802-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="50802-104">SYNTAX</span></span>

### <span data-ttu-id="50802-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="50802-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50802-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="50802-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Eventhub] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50802-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="50802-107">AliasAuthoRuleSet</span></span>
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50802-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="50802-108">DESCRIPTION</span></span>
<span data-ttu-id="50802-109">Командлет Get-AzureRmEventHubAuthorizationRule получает либо сведения о правиле авторизации, либо список всех правил авторизации для определенного концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="50802-109">The Get-AzureRmEventHubAuthorizationRule cmdlet gets either the details of an authorization rule, or a list of all authorization rules for a specified Event Hub.</span></span>
<span data-ttu-id="50802-110">Если указано имя правила авторизации, возвращается информация об этом отдельном правиле авторизации.</span><span class="sxs-lookup"><span data-stu-id="50802-110">If the name of an authorization rule is provided, the details of that single authorization rule are returned.</span></span>
<span data-ttu-id="50802-111">Если имя правила авторизации не задано, возвращается список всех правил авторизации для указанного концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="50802-111">If the name of an authorization rule is not provided, a list of all authorization rules for the specified Event Hub is returned.</span></span>
<span data-ttu-id="50802-112">Если задано имя псевдонима (аварийное восстановление), возвращается информация о правиле авторизации пространства имен для указанного псевдонима.</span><span class="sxs-lookup"><span data-stu-id="50802-112">If (Disaster Recovery) Alias name provided, the details of authorization rule of the Namespace for Alias configured is returned.</span></span> 

## <span data-ttu-id="50802-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="50802-113">EXAMPLES</span></span>

### <span data-ttu-id="50802-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="50802-114">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRule MyAuthRuleName
```

<span data-ttu-id="50802-115">Получает правило авторизации \` MyAuthRuleName \` в MyEventHubName концентратора событий \` \` , область которого ограничена пространством имен \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="50802-115">Gets the authorization rule \`MyAuthRuleName\` in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="50802-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="50802-116">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="50802-117">Получает список всех правил авторизации в концентраторе событий \` MyEventHubName \` , область которого ограничена пространством имен \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="50802-117">Gets a list of all authorization rules in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="50802-118">Пример 3</span><span class="sxs-lookup"><span data-stu-id="50802-118">Example 3</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName -Name MyAuthRuleName
```

<span data-ttu-id="50802-119">Возвращает правило авторизации \` , MyAuthRuleName \` в пространстве имен \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="50802-119">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="50802-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="50802-120">PARAMETERS</span></span>

### <span data-ttu-id="50802-121">-AliasName</span><span class="sxs-lookup"><span data-stu-id="50802-121">-AliasName</span></span>
<span data-ttu-id="50802-122">Имя псевдонима</span><span class="sxs-lookup"><span data-stu-id="50802-122">Alias Name</span></span>

```yaml
Type: String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50802-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50802-123">-DefaultProfile</span></span>
<span data-ttu-id="50802-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="50802-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50802-125">-Eventhub</span><span class="sxs-lookup"><span data-stu-id="50802-125">-Eventhub</span></span>
<span data-ttu-id="50802-126">Имя Eventhub</span><span class="sxs-lookup"><span data-stu-id="50802-126">Eventhub Name</span></span>

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

### <span data-ttu-id="50802-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="50802-127">-Name</span></span>
<span data-ttu-id="50802-128">Имя AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="50802-128">AuthorizationRule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50802-129">-Namespace</span><span class="sxs-lookup"><span data-stu-id="50802-129">-Namespace</span></span>
<span data-ttu-id="50802-130">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="50802-130">Namespace Name</span></span>

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

### <span data-ttu-id="50802-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50802-131">-ResourceGroupName</span></span>
<span data-ttu-id="50802-132">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="50802-132">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50802-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50802-133">CommonParameters</span></span>
<span data-ttu-id="50802-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="50802-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="50802-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50802-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50802-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="50802-136">INPUTS</span></span>

### <span data-ttu-id="50802-137">System. String</span><span class="sxs-lookup"><span data-stu-id="50802-137">System.String</span></span>


## <span data-ttu-id="50802-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="50802-138">OUTPUTS</span></span>

### <span data-ttu-id="50802-139">System. Collections. Generic. List "1 [[Microsoft. Azure. Commands. eventhub, версия = 0.5.0.0, культура = нейтраль, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="50802-139">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.EventHub, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="50802-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="50802-140">NOTES</span></span>

## <span data-ttu-id="50802-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="50802-141">RELATED LINKS</span></span>
