---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubKey.md
ms.openlocfilehash: c22bb41702bb4e338d0548be6c7544d597ef0230
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566815"
---
# <span data-ttu-id="273ae-101">Get-AzureRmEventHubKey</span><span class="sxs-lookup"><span data-stu-id="273ae-101">Get-AzureRmEventHubKey</span></span>

## <span data-ttu-id="273ae-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="273ae-102">SYNOPSIS</span></span>
<span data-ttu-id="273ae-103">Возвращает сведения о первичном ключе для указанного правила авторизации концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="273ae-103">Gets the primary key details of the specified Event Hubs authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="273ae-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="273ae-104">SYNTAX</span></span>

### <span data-ttu-id="273ae-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="273ae-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="273ae-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="273ae-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="273ae-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="273ae-107">AliasAuthoRuleSet</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="273ae-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="273ae-108">DESCRIPTION</span></span>
<span data-ttu-id="273ae-109">Командлет Get-AzureRmEventHubKey возвращает первичные и вторичные ConnectionString и сведения о нем для указанного пространства имен, концентраторов событий и псевдонимов.</span><span class="sxs-lookup"><span data-stu-id="273ae-109">The Get-AzureRmEventHubKey cmdlet returns Primary and Secondary connectionstrings and keys details of the specified NameSpace/Event Hubs/Alias authorization rule.</span></span>

## <span data-ttu-id="273ae-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="273ae-110">EXAMPLES</span></span>

### <span data-ttu-id="273ae-111">Пример 1 — пространство имен</span><span class="sxs-lookup"><span data-stu-id="273ae-111">Example 1 - Namespace</span></span>
```
PS C:\> Get-AzureRmEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

### <span data-ttu-id="273ae-112">Пример 2-EventHub</span><span class="sxs-lookup"><span data-stu-id="273ae-112">Example 2 - EventHub</span></span>
```
PS C:\> Get-AzureRmEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="273ae-113">Получение подробных сведений о первичных и вспомогательных элементах ConnectionString и ключах для правила авторизации \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="273ae-113">Gets details of Primary and Secondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="273ae-114">Пример 3-псевдоним (конфигурация с геовосстановлением)</span><span class="sxs-lookup"><span data-stu-id="273ae-114">Example 3 - Alias (GeoRecovery Configuration)</span></span>
```
PS C:\> Get-AzureRmEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AliasName MyAliasName -Name MyAuthRuleName
```

<span data-ttu-id="273ae-115">Получение сведений о первичных, вспомогательных, AliasPrimary и AliasSecondary ConnectionString и ключах для правила авторизации \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="273ae-115">Gets details of Primary, Secondary, AliasPrimary and AliasSecondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="273ae-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="273ae-116">PARAMETERS</span></span>

### <span data-ttu-id="273ae-117">-AliasName</span><span class="sxs-lookup"><span data-stu-id="273ae-117">-AliasName</span></span>
<span data-ttu-id="273ae-118">Имя псевдонима</span><span class="sxs-lookup"><span data-stu-id="273ae-118">Alias Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="273ae-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="273ae-119">-DefaultProfile</span></span>
<span data-ttu-id="273ae-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="273ae-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="273ae-121">-EventHub</span><span class="sxs-lookup"><span data-stu-id="273ae-121">-EventHub</span></span>
<span data-ttu-id="273ae-122">Имя EventHub</span><span class="sxs-lookup"><span data-stu-id="273ae-122">EventHub Name</span></span>

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

### <span data-ttu-id="273ae-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="273ae-123">-Name</span></span>
<span data-ttu-id="273ae-124">Имя AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="273ae-124">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="273ae-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="273ae-125">-Namespace</span></span>
<span data-ttu-id="273ae-126">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="273ae-126">Namespace Name</span></span>

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

### <span data-ttu-id="273ae-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="273ae-127">-ResourceGroupName</span></span>
<span data-ttu-id="273ae-128">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="273ae-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="273ae-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="273ae-129">CommonParameters</span></span>
<span data-ttu-id="273ae-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="273ae-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="273ae-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="273ae-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="273ae-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="273ae-132">INPUTS</span></span>

### <span data-ttu-id="273ae-133">System. String</span><span class="sxs-lookup"><span data-stu-id="273ae-133">System.String</span></span>

## <span data-ttu-id="273ae-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="273ae-134">OUTPUTS</span></span>

### <span data-ttu-id="273ae-135">Microsoft. Azure. Commands. EventHub. Models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="273ae-135">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="273ae-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="273ae-136">NOTES</span></span>

## <span data-ttu-id="273ae-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="273ae-137">RELATED LINKS</span></span>
