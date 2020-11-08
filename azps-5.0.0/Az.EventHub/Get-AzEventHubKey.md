---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubKey.md
ms.openlocfilehash: 0b77c4e4329577443e37054ce9861e246720e706
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248687"
---
# <span data-ttu-id="e2ef4-101">Get-AzEventHubKey</span><span class="sxs-lookup"><span data-stu-id="e2ef4-101">Get-AzEventHubKey</span></span>

## <span data-ttu-id="e2ef4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e2ef4-102">SYNOPSIS</span></span>
<span data-ttu-id="e2ef4-103">Возвращает сведения о первичном ключе для указанного правила авторизации концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="e2ef4-103">Gets the primary key details of the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="e2ef4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e2ef4-104">SYNTAX</span></span>

### <span data-ttu-id="e2ef4-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e2ef4-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2ef4-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="e2ef4-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2ef4-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="e2ef4-107">AliasAuthoRuleSet</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2ef4-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2ef4-108">DESCRIPTION</span></span>
<span data-ttu-id="e2ef4-109">Командлет Get-AzEventHubKey возвращает первичные и вторичные ConnectionString и сведения о нем для указанного пространства имен, концентраторов событий и псевдонимов.</span><span class="sxs-lookup"><span data-stu-id="e2ef4-109">The Get-AzEventHubKey cmdlet returns Primary and Secondary connectionstrings and keys details of the specified NameSpace/Event Hubs/Alias authorization rule.</span></span>

## <span data-ttu-id="e2ef4-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e2ef4-110">EXAMPLES</span></span>

### <span data-ttu-id="e2ef4-111">Пример 1: пространство имен</span><span class="sxs-lookup"><span data-stu-id="e2ef4-111">Example 1: Namespace</span></span>
```powershell
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

### <span data-ttu-id="e2ef4-112">Пример 2: EventHub</span><span class="sxs-lookup"><span data-stu-id="e2ef4-112">Example 2: EventHub</span></span>
```powershell
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="e2ef4-113">Получение подробных сведений о первичных и вспомогательных элементах ConnectionString и ключах для правила авторизации \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="e2ef4-113">Gets details of Primary and Secondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="e2ef4-114">Пример 3: псевдоним (конфигурация с геовосстановлением)</span><span class="sxs-lookup"><span data-stu-id="e2ef4-114">Example 3: Alias (GeoRecovery Configuration)</span></span>
```powershell
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AliasName MyAliasName -Name MyAuthRuleName
```

<span data-ttu-id="e2ef4-115">Получение сведений о первичных, вспомогательных, AliasPrimary и AliasSecondary ConnectionString и ключах для правила авторизации \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="e2ef4-115">Gets details of Primary, Secondary, AliasPrimary and AliasSecondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="e2ef4-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e2ef4-116">PARAMETERS</span></span>

### <span data-ttu-id="e2ef4-117">-AliasName</span><span class="sxs-lookup"><span data-stu-id="e2ef4-117">-AliasName</span></span>
<span data-ttu-id="e2ef4-118">Имя псевдонима</span><span class="sxs-lookup"><span data-stu-id="e2ef4-118">Alias Name</span></span>

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

### <span data-ttu-id="e2ef4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2ef4-119">-DefaultProfile</span></span>
<span data-ttu-id="e2ef4-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e2ef4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2ef4-121">-EventHub</span><span class="sxs-lookup"><span data-stu-id="e2ef4-121">-EventHub</span></span>
<span data-ttu-id="e2ef4-122">Имя EventHub</span><span class="sxs-lookup"><span data-stu-id="e2ef4-122">EventHub Name</span></span>

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

### <span data-ttu-id="e2ef4-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e2ef4-123">-Name</span></span>
<span data-ttu-id="e2ef4-124">Имя AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e2ef4-124">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="e2ef4-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e2ef4-125">-Namespace</span></span>
<span data-ttu-id="e2ef4-126">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="e2ef4-126">Namespace Name</span></span>

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

### <span data-ttu-id="e2ef4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2ef4-127">-ResourceGroupName</span></span>
<span data-ttu-id="e2ef4-128">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="e2ef4-128">Resource Group Name</span></span>

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

### <span data-ttu-id="e2ef4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2ef4-129">CommonParameters</span></span>
<span data-ttu-id="e2ef4-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e2ef4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2ef4-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2ef4-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2ef4-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e2ef4-132">INPUTS</span></span>

### <span data-ttu-id="e2ef4-133">System. String</span><span class="sxs-lookup"><span data-stu-id="e2ef4-133">System.String</span></span>

## <span data-ttu-id="e2ef4-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2ef4-134">OUTPUTS</span></span>

### <span data-ttu-id="e2ef4-135">Microsoft. Azure. Commands. EventHub. Models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="e2ef4-135">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="e2ef4-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="e2ef4-136">NOTES</span></span>

## <span data-ttu-id="e2ef4-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e2ef4-137">RELATED LINKS</span></span>
