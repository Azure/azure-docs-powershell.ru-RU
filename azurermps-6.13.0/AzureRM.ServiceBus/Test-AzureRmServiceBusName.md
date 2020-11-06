---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/test-azurermservicebusname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
ms.openlocfilehash: e7fafeeee8a377cc9bb7eb9ce514c0a0d7b89c9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562607"
---
# <span data-ttu-id="9f718-101">Test-AzureRmServiceBusName</span><span class="sxs-lookup"><span data-stu-id="9f718-101">Test-AzureRmServiceBusName</span></span>

## <span data-ttu-id="9f718-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9f718-102">SYNOPSIS</span></span>
<span data-ttu-id="9f718-103">Проверяет доступность указанного имени пространства имен или псевдонима (имя конфигурации DR).</span><span class="sxs-lookup"><span data-stu-id="9f718-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f718-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9f718-104">SYNTAX</span></span>

### <span data-ttu-id="9f718-105">AliasCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="9f718-105">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzureRmServiceBusName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f718-106">NamespaceCheckNameAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="9f718-106">NamespaceCheckNameAvailabilitySet</span></span>
```
Test-AzureRmServiceBusName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9f718-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f718-107">DESCRIPTION</span></span>
<span data-ttu-id="9f718-108">Командлет **Test-AzureRmServiceBusName** проверяет доступность имени или псевдонима пространства имен (имя конфигурации DR).</span><span class="sxs-lookup"><span data-stu-id="9f718-108">The **Test-AzureRmServiceBusName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="9f718-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9f718-109">EXAMPLES</span></span>

### <span data-ttu-id="9f718-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9f718-110">Example 1</span></span>
```
PS C:\> Test-AzureRmServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="9f718-111">Возвращает состояние доступности имени пространства имен "MyNameSapceName" как истина.</span><span class="sxs-lookup"><span data-stu-id="9f718-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True</span></span>

### <span data-ttu-id="9f718-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="9f718-112">Example 2</span></span>
```
PS C:\> Test-AzureRmServiceBusName -Namespace MyNameSapceName
```

<span data-ttu-id="9f718-113">Возвращает состояние доступности имени пространства имен "MyNameSapceName" как false с указанием причины</span><span class="sxs-lookup"><span data-stu-id="9f718-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="9f718-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="9f718-114">Example 3</span></span>
```
PS C:\> Test-AzureRmServiceBusName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

## <span data-ttu-id="9f718-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9f718-115">PARAMETERS</span></span>

### <span data-ttu-id="9f718-116">-AliasName</span><span class="sxs-lookup"><span data-stu-id="9f718-116">-AliasName</span></span>
<span data-ttu-id="9f718-117">Имя конфигурации DR — имя псевдонима</span><span class="sxs-lookup"><span data-stu-id="9f718-117">DR Configuration Name - Alias Name</span></span>

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

### <span data-ttu-id="9f718-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f718-118">-DefaultProfile</span></span>
<span data-ttu-id="9f718-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9f718-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f718-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="9f718-120">-Namespace</span></span>
<span data-ttu-id="9f718-121">Имя пространства имен servicebus</span><span class="sxs-lookup"><span data-stu-id="9f718-121">Servicebus Namespace Name</span></span>

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

### <span data-ttu-id="9f718-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f718-122">-ResourceGroupName</span></span>
<span data-ttu-id="9f718-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="9f718-123">Resource Group Name</span></span>

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

### <span data-ttu-id="9f718-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f718-124">CommonParameters</span></span>
<span data-ttu-id="9f718-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9f718-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f718-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f718-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f718-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9f718-127">INPUTS</span></span>

### <span data-ttu-id="9f718-128">System. String</span><span class="sxs-lookup"><span data-stu-id="9f718-128">System.String</span></span>

## <span data-ttu-id="9f718-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f718-129">OUTPUTS</span></span>

### <span data-ttu-id="9f718-130">Microsoft. Azure. Commands. ServiceBus. Models. PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="9f718-130">Microsoft.Azure.Commands.ServiceBus.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="9f718-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="9f718-131">NOTES</span></span>

## <span data-ttu-id="9f718-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9f718-132">RELATED LINKS</span></span>
