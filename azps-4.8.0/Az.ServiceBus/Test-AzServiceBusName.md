---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/test-azservicebusname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusName.md
ms.openlocfilehash: a52274d44b36f2e0dea220464ba835635ab845f4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077591"
---
# <span data-ttu-id="4c625-101">Test-AzServiceBusName</span><span class="sxs-lookup"><span data-stu-id="4c625-101">Test-AzServiceBusName</span></span>

## <span data-ttu-id="4c625-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4c625-102">SYNOPSIS</span></span>
<span data-ttu-id="4c625-103">Проверяет доступность указанного имени пространства имен или псевдонима (имя конфигурации DR).</span><span class="sxs-lookup"><span data-stu-id="4c625-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span> 

## <span data-ttu-id="4c625-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4c625-104">SYNTAX</span></span>

### <span data-ttu-id="4c625-105">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="4c625-105">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c625-106">NamespaceCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="4c625-106">NamespaceCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c625-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4c625-107">DESCRIPTION</span></span>
<span data-ttu-id="4c625-108">Командлет **Test-AzServiceBusName** проверяет доступность имени или псевдонима пространства имен (имя конфигурации DR).</span><span class="sxs-lookup"><span data-stu-id="4c625-108">The **Test-AzServiceBusName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="4c625-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4c625-109">EXAMPLES</span></span>

### <span data-ttu-id="4c625-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4c625-110">Example 1</span></span>
```
PS C:\> Test-AzServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="4c625-111">Возвращает состояние доступности имени пространства имен "MyNameSapceName" как истина.</span><span class="sxs-lookup"><span data-stu-id="4c625-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True</span></span>

### <span data-ttu-id="4c625-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="4c625-112">Example 2</span></span>
```
PS C:\> Test-AzServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="4c625-113">Возвращает состояние доступности имени пространства имен "MyNameSapceName" как false с указанием причины</span><span class="sxs-lookup"><span data-stu-id="4c625-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="4c625-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="4c625-114">Example 3</span></span>
```
PS C:\> Test-AzServiceBusName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

## <span data-ttu-id="4c625-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4c625-115">PARAMETERS</span></span>

### <span data-ttu-id="4c625-116">-AliasName</span><span class="sxs-lookup"><span data-stu-id="4c625-116">-AliasName</span></span>
<span data-ttu-id="4c625-117">Имя конфигурации DR — имя псевдонима</span><span class="sxs-lookup"><span data-stu-id="4c625-117">DR Configuration Name - Alias Name</span></span>

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

### <span data-ttu-id="4c625-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c625-118">-DefaultProfile</span></span>
<span data-ttu-id="4c625-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4c625-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c625-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4c625-120">-Namespace</span></span>
<span data-ttu-id="4c625-121">Имя пространства имен servicebus</span><span class="sxs-lookup"><span data-stu-id="4c625-121">Servicebus Namespace Name</span></span>

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

### <span data-ttu-id="4c625-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c625-122">-ResourceGroupName</span></span>
<span data-ttu-id="4c625-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="4c625-123">Resource Group Name</span></span>

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

### <span data-ttu-id="4c625-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c625-124">CommonParameters</span></span>
<span data-ttu-id="4c625-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4c625-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c625-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c625-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c625-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4c625-127">INPUTS</span></span>

### <span data-ttu-id="4c625-128">System. String</span><span class="sxs-lookup"><span data-stu-id="4c625-128">System.String</span></span>

## <span data-ttu-id="4c625-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4c625-129">OUTPUTS</span></span>

### <span data-ttu-id="4c625-130">Microsoft. Azure. Commands. ServiceBus. Models. PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="4c625-130">Microsoft.Azure.Commands.ServiceBus.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="4c625-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="4c625-131">NOTES</span></span>

## <span data-ttu-id="4c625-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4c625-132">RELATED LINKS</span></span>
