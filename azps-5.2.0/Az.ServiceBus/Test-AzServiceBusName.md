---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/test-azservicebusname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusName.md
ms.openlocfilehash: a52274d44b36f2e0dea220464ba835635ab845f4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98415956"
---
# <span data-ttu-id="5f428-101">Test-AzServiceBusName</span><span class="sxs-lookup"><span data-stu-id="5f428-101">Test-AzServiceBusName</span></span>

## <span data-ttu-id="5f428-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f428-102">SYNOPSIS</span></span>
<span data-ttu-id="5f428-103">Проверка доступности заданного имени или псевдонима пространства имен (ИМЯ конфигурации DR)</span><span class="sxs-lookup"><span data-stu-id="5f428-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span> 

## <span data-ttu-id="5f428-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5f428-104">SYNTAX</span></span>

### <span data-ttu-id="5f428-105">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="5f428-105">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f428-106">NamespaceCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="5f428-106">NamespaceCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f428-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5f428-107">DESCRIPTION</span></span>
<span data-ttu-id="5f428-108">Проверка доступности имени или псевдонима пространства имен (DR Configuration NameSpace) в **cmdlet AzServiceBusName**</span><span class="sxs-lookup"><span data-stu-id="5f428-108">The **Test-AzServiceBusName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="5f428-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5f428-109">EXAMPLES</span></span>

### <span data-ttu-id="5f428-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5f428-110">Example 1</span></span>
```
PS C:\> Test-AzServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="5f428-111">Возвращает состояние доступности имени пространства имен MyNameSapceName как True.</span><span class="sxs-lookup"><span data-stu-id="5f428-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True</span></span>

### <span data-ttu-id="5f428-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5f428-112">Example 2</span></span>
```
PS C:\> Test-AzServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="5f428-113">Возвращает состояние доступности имени пространства имен "MyNameSapceName" как "False" с причиной.</span><span class="sxs-lookup"><span data-stu-id="5f428-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="5f428-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="5f428-114">Example 3</span></span>
```
PS C:\> Test-AzServiceBusName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

## <span data-ttu-id="5f428-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5f428-115">PARAMETERS</span></span>

### <span data-ttu-id="5f428-116">-AliasName</span><span class="sxs-lookup"><span data-stu-id="5f428-116">-AliasName</span></span>
<span data-ttu-id="5f428-117">Имя конфигурации DR — имя псевдонима</span><span class="sxs-lookup"><span data-stu-id="5f428-117">DR Configuration Name - Alias Name</span></span>

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

### <span data-ttu-id="5f428-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f428-118">-DefaultProfile</span></span>
<span data-ttu-id="5f428-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5f428-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f428-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5f428-120">-Namespace</span></span>
<span data-ttu-id="5f428-121">Имя пространства имен servicebus</span><span class="sxs-lookup"><span data-stu-id="5f428-121">Servicebus Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f428-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f428-122">-ResourceGroupName</span></span>
<span data-ttu-id="5f428-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="5f428-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f428-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f428-124">CommonParameters</span></span>
<span data-ttu-id="5f428-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f428-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f428-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f428-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f428-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5f428-127">INPUTS</span></span>

### <span data-ttu-id="5f428-128">System.String</span><span class="sxs-lookup"><span data-stu-id="5f428-128">System.String</span></span>

## <span data-ttu-id="5f428-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5f428-129">OUTPUTS</span></span>

### <span data-ttu-id="5f428-130">Microsoft.Azure.Commands.ServiceBus.Models.PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="5f428-130">Microsoft.Azure.Commands.ServiceBus.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="5f428-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5f428-131">NOTES</span></span>

## <span data-ttu-id="5f428-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5f428-132">RELATED LINKS</span></span>
