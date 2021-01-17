---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubKey.md
ms.openlocfilehash: 0b77c4e4329577443e37054ce9861e246720e706
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323557"
---
# <span data-ttu-id="3739d-101">Get-AzEventHubKey</span><span class="sxs-lookup"><span data-stu-id="3739d-101">Get-AzEventHubKey</span></span>

## <span data-ttu-id="3739d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3739d-102">SYNOPSIS</span></span>
<span data-ttu-id="3739d-103">Возвращает сведения о первичном ключе для заданного правила авторизации "Концентраторы событий".</span><span class="sxs-lookup"><span data-stu-id="3739d-103">Gets the primary key details of the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="3739d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3739d-104">SYNTAX</span></span>

### <span data-ttu-id="3739d-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3739d-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3739d-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="3739d-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3739d-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="3739d-107">AliasAuthoRuleSet</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3739d-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3739d-108">DESCRIPTION</span></span>
<span data-ttu-id="3739d-109">Этот Get-AzEventHubKey возвращает основные и дополнительные части подключения и ключи для указанного правила авторизации NameSpace/Event Hubs/Alias.</span><span class="sxs-lookup"><span data-stu-id="3739d-109">The Get-AzEventHubKey cmdlet returns Primary and Secondary connectionstrings and keys details of the specified NameSpace/Event Hubs/Alias authorization rule.</span></span>

## <span data-ttu-id="3739d-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3739d-110">EXAMPLES</span></span>

### <span data-ttu-id="3739d-111">Пример 1. Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3739d-111">Example 1: Namespace</span></span>
```powershell
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

### <span data-ttu-id="3739d-112">Пример 2. EventHub</span><span class="sxs-lookup"><span data-stu-id="3739d-112">Example 2: EventHub</span></span>
```powershell
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="3739d-113">Сведения о первичных и дополнительных подключениях и ключах для правила авторизации \` MyAuthRuleName. \`</span><span class="sxs-lookup"><span data-stu-id="3739d-113">Gets details of Primary and Secondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="3739d-114">Пример 3. Псевдоним (конфигурация geoRecovery)</span><span class="sxs-lookup"><span data-stu-id="3739d-114">Example 3: Alias (GeoRecovery Configuration)</span></span>
```powershell
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AliasName MyAliasName -Name MyAuthRuleName
```

<span data-ttu-id="3739d-115">Сведения о первичных, дополнительных, псевдонимахPrimary и AliasSecondary connectionstrings и ключах для правила авторизации \` MyAuthRuleName. \`</span><span class="sxs-lookup"><span data-stu-id="3739d-115">Gets details of Primary, Secondary, AliasPrimary and AliasSecondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="3739d-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3739d-116">PARAMETERS</span></span>

### <span data-ttu-id="3739d-117">-AliasName</span><span class="sxs-lookup"><span data-stu-id="3739d-117">-AliasName</span></span>
<span data-ttu-id="3739d-118">Alias Name</span><span class="sxs-lookup"><span data-stu-id="3739d-118">Alias Name</span></span>

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

### <span data-ttu-id="3739d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3739d-119">-DefaultProfile</span></span>
<span data-ttu-id="3739d-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3739d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3739d-121">-EventHub</span><span class="sxs-lookup"><span data-stu-id="3739d-121">-EventHub</span></span>
<span data-ttu-id="3739d-122">EventHub Name</span><span class="sxs-lookup"><span data-stu-id="3739d-122">EventHub Name</span></span>

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

### <span data-ttu-id="3739d-123">-Name</span><span class="sxs-lookup"><span data-stu-id="3739d-123">-Name</span></span>
<span data-ttu-id="3739d-124">Имяrule authorizationRule</span><span class="sxs-lookup"><span data-stu-id="3739d-124">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="3739d-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3739d-125">-Namespace</span></span>
<span data-ttu-id="3739d-126">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="3739d-126">Namespace Name</span></span>

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

### <span data-ttu-id="3739d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3739d-127">-ResourceGroupName</span></span>
<span data-ttu-id="3739d-128">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="3739d-128">Resource Group Name</span></span>

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

### <span data-ttu-id="3739d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3739d-129">CommonParameters</span></span>
<span data-ttu-id="3739d-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3739d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3739d-131">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3739d-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3739d-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3739d-132">INPUTS</span></span>

### <span data-ttu-id="3739d-133">System.String</span><span class="sxs-lookup"><span data-stu-id="3739d-133">System.String</span></span>

## <span data-ttu-id="3739d-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3739d-134">OUTPUTS</span></span>

### <span data-ttu-id="3739d-135">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="3739d-135">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="3739d-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3739d-136">NOTES</span></span>

## <span data-ttu-id="3739d-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3739d-137">RELATED LINKS</span></span>
