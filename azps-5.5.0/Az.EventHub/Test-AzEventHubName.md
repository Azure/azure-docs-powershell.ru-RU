---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/test-azeventhubname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Test-AzEventHubName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Test-AzEventHubName.md
ms.openlocfilehash: 8eb43982db0eddeb9127006e0cfa3336698eb7e3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100237843"
---
# <span data-ttu-id="84575-101">Test-AzEventHubName</span><span class="sxs-lookup"><span data-stu-id="84575-101">Test-AzEventHubName</span></span>

## <span data-ttu-id="84575-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84575-102">SYNOPSIS</span></span>
<span data-ttu-id="84575-103">Проверка доступности заданного имени или псевдонима пространства имен (ИМЯ конфигурации DR)</span><span class="sxs-lookup"><span data-stu-id="84575-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="84575-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="84575-104">SYNTAX</span></span>

### <span data-ttu-id="84575-105">NamespaceCheckNameAvailabilitySet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="84575-105">NamespaceCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzEventHubName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84575-106">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="84575-106">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzEventHubName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84575-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="84575-107">DESCRIPTION</span></span>
<span data-ttu-id="84575-108">Проверка доступности имени или псевдонима (псевдонима DR Configuration) в окне **Test-AzEventhubName**</span><span class="sxs-lookup"><span data-stu-id="84575-108">The **Test-AzEventhubName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="84575-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="84575-109">EXAMPLES</span></span>

### <span data-ttu-id="84575-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="84575-110">Example 1</span></span>
```
PS C:\> Test-AzEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="84575-111">Возвращает состояние доступности имени пространства имен "MyNameSapceName" как "Истина", если доступно.</span><span class="sxs-lookup"><span data-stu-id="84575-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True if available</span></span>

### <span data-ttu-id="84575-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="84575-112">Example 2</span></span>
```
PS C:\> Test-AzEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="84575-113">Возвращает состояние доступности имени пространства имен "MyNameSapceName" как "False" с причиной.</span><span class="sxs-lookup"><span data-stu-id="84575-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="84575-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="84575-114">Example 3</span></span>
```
PS C:\> Test-AzEventhubName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

<span data-ttu-id="84575-115">Возвращает состояние доступности псевдонимного имени "myAliasName" в области имен "MyNameSapceName" как "True", если доступно.</span><span class="sxs-lookup"><span data-stu-id="84575-115">Returns the status on availability of the alias name 'myAliasName' for namespace 'MyNameSapceName' as True if available</span></span>

## <span data-ttu-id="84575-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="84575-116">PARAMETERS</span></span>

### <span data-ttu-id="84575-117">-AliasName</span><span class="sxs-lookup"><span data-stu-id="84575-117">-AliasName</span></span>
<span data-ttu-id="84575-118">Имя конфигурации DR — имя псевдонима</span><span class="sxs-lookup"><span data-stu-id="84575-118">DR Configuration Name - Alias Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84575-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84575-119">-DefaultProfile</span></span>
<span data-ttu-id="84575-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="84575-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84575-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="84575-121">-Namespace</span></span>
<span data-ttu-id="84575-122">Имя пространства имен Eventhub</span><span class="sxs-lookup"><span data-stu-id="84575-122">Eventhub Namespace Name</span></span>

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

### <span data-ttu-id="84575-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84575-123">-ResourceGroupName</span></span>
<span data-ttu-id="84575-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="84575-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84575-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84575-125">CommonParameters</span></span>
<span data-ttu-id="84575-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84575-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84575-127">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84575-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84575-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="84575-128">INPUTS</span></span>

### <span data-ttu-id="84575-129">System.String</span><span class="sxs-lookup"><span data-stu-id="84575-129">System.String</span></span>

## <span data-ttu-id="84575-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="84575-130">OUTPUTS</span></span>

### <span data-ttu-id="84575-131">Microsoft.Azure.Commands.EventHub.Models.PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="84575-131">Microsoft.Azure.Commands.EventHub.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="84575-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="84575-132">NOTES</span></span>

## <span data-ttu-id="84575-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="84575-133">RELATED LINKS</span></span>
