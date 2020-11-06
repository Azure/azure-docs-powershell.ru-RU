---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/test-azurermservicebusname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
ms.openlocfilehash: a35487b2eb1dae8d8af452fba9a47854ecab6efb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561464"
---
# <span data-ttu-id="87f83-101">Test-AzureRmServiceBusName</span><span class="sxs-lookup"><span data-stu-id="87f83-101">Test-AzureRmServiceBusName</span></span>

## <span data-ttu-id="87f83-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="87f83-102">SYNOPSIS</span></span>
<span data-ttu-id="87f83-103">Проверяет доступность указанного имени пространства имен или псевдонима (имя конфигурации DR).</span><span class="sxs-lookup"><span data-stu-id="87f83-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87f83-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="87f83-104">SYNTAX</span></span>

### <span data-ttu-id="87f83-105">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="87f83-105">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzureRmServiceBusName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87f83-106">NamespaceCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="87f83-106">NamespaceCheckNameAvailabilitySet</span></span>
```
Test-AzureRmServiceBusName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="87f83-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="87f83-107">DESCRIPTION</span></span>
<span data-ttu-id="87f83-108">Командлет **Test-AzureRmServiceBusName** проверяет доступность имени или псевдонима пространства имен (имя конфигурации DR).</span><span class="sxs-lookup"><span data-stu-id="87f83-108">The **Test-AzureRmServiceBusName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="87f83-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="87f83-109">EXAMPLES</span></span>

### <span data-ttu-id="87f83-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="87f83-110">Example 1</span></span>
```
PS C:\> Test-AzureRmServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="87f83-111">Возвращает состояние доступности имени пространства имен "MyNameSapceName" как истина.</span><span class="sxs-lookup"><span data-stu-id="87f83-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True</span></span>

### <span data-ttu-id="87f83-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="87f83-112">Example 2</span></span>
```
PS C:\> Test-AzureRmServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="87f83-113">Возвращает состояние доступности имени пространства имен "MyNameSapceName" как false с указанием причины</span><span class="sxs-lookup"><span data-stu-id="87f83-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="87f83-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="87f83-114">Example 3</span></span>
```
PS C:\> Test-AzureRmServiceBusName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```


## <span data-ttu-id="87f83-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="87f83-115">PARAMETERS</span></span>

### <span data-ttu-id="87f83-116">-AliasName</span><span class="sxs-lookup"><span data-stu-id="87f83-116">-AliasName</span></span>
<span data-ttu-id="87f83-117">Имя конфигурации DR — имя псевдонима</span><span class="sxs-lookup"><span data-stu-id="87f83-117">DR Configuration Name - Alias Name</span></span>

```yaml
Type: String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases: Alias

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87f83-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87f83-118">-DefaultProfile</span></span>
<span data-ttu-id="87f83-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="87f83-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87f83-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="87f83-120">-Namespace</span></span>
<span data-ttu-id="87f83-121">Имя пространства имен servicebus</span><span class="sxs-lookup"><span data-stu-id="87f83-121">Servicebus Namespace Name</span></span>

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

### <span data-ttu-id="87f83-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87f83-122">-ResourceGroupName</span></span>
<span data-ttu-id="87f83-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="87f83-123">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87f83-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87f83-124">CommonParameters</span></span>
<span data-ttu-id="87f83-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="87f83-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="87f83-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87f83-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87f83-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="87f83-127">INPUTS</span></span>

### <span data-ttu-id="87f83-128">System. String</span><span class="sxs-lookup"><span data-stu-id="87f83-128">System.String</span></span>


## <span data-ttu-id="87f83-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="87f83-129">OUTPUTS</span></span>

### <span data-ttu-id="87f83-130">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. ServiceBus. Models. PSCheckNameAvailabilityResultAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.5.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="87f83-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.PSCheckNameAvailabilityResultAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="87f83-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="87f83-131">NOTES</span></span>

## <span data-ttu-id="87f83-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="87f83-132">RELATED LINKS</span></span>
