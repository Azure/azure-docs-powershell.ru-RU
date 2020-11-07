---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
ms.openlocfilehash: 892177efebb3a62e40f79b80b1ac67c488e048d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734225"
---
# <span data-ttu-id="558c0-101">Test-AzureRmServiceBusName</span><span class="sxs-lookup"><span data-stu-id="558c0-101">Test-AzureRmServiceBusName</span></span>

## <span data-ttu-id="558c0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="558c0-102">SYNOPSIS</span></span>
<span data-ttu-id="558c0-103">Проверяет доступность указанного имени пространства имен.</span><span class="sxs-lookup"><span data-stu-id="558c0-103">Checks the Availability of the given NameSpace Name</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="558c0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="558c0-104">SYNTAX</span></span>

```
Test-AzureRmServiceBusName [-Namespace] <String>
```

## <span data-ttu-id="558c0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="558c0-105">DESCRIPTION</span></span>
<span data-ttu-id="558c0-106">Командлет **Test-AzureRmServiceBusName** проверяет доступность имени пространства имен</span><span class="sxs-lookup"><span data-stu-id="558c0-106">The **Test-AzureRmServiceBusName** Cmdlet Check Availability of the NameSpace Name</span></span>

## <span data-ttu-id="558c0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="558c0-107">EXAMPLES</span></span>

### <span data-ttu-id="558c0-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="558c0-108">Example 1</span></span>
```
PS C:\> Test-AzureRmServiceBusName -Namespace TestingtheAvailability
```

### <span data-ttu-id="558c0-109">Пример 2</span><span class="sxs-lookup"><span data-stu-id="558c0-109">Example 2</span></span>
```
PS C:\> Test-AzureRmServiceBusName -Namespace Testi
```

### <span data-ttu-id="558c0-110">Пример 3</span><span class="sxs-lookup"><span data-stu-id="558c0-110">Example 3</span></span>
```
PS C:\> Test-AzureRmServiceBusName -Namespace Test123
```

<span data-ttu-id="558c0-111">Возвращает состояние доступности имени пространства имен.</span><span class="sxs-lookup"><span data-stu-id="558c0-111">Returns the status on availability of the namespace name</span></span>

## <span data-ttu-id="558c0-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="558c0-112">PARAMETERS</span></span>

### <span data-ttu-id="558c0-113">-Namespace</span><span class="sxs-lookup"><span data-stu-id="558c0-113">-Namespace</span></span>
<span data-ttu-id="558c0-114">Имя пространства имен ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="558c0-114">ServiceBus Namespace Name.</span></span>

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
### <span data-ttu-id="558c0-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="558c0-115">CommonParameters</span></span>
<span data-ttu-id="558c0-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="558c0-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="558c0-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="558c0-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="558c0-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="558c0-118">INPUTS</span></span>

### <span data-ttu-id="558c0-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="558c0-119">-Namespace</span></span>
 <span data-ttu-id="558c0-120">System. String</span><span class="sxs-lookup"><span data-stu-id="558c0-120">System.String</span></span>

## <span data-ttu-id="558c0-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="558c0-121">OUTPUTS</span></span>

### <span data-ttu-id="558c0-122">[Microsoft. Azure. Commands. ServiceBus. Models. CheckNameAvailabilityResultAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.1.0.0, культура = Neutral, PublicKeyToken = NULL]</span><span class="sxs-lookup"><span data-stu-id="558c0-122">[Microsoft.Azure.Commands.ServiceBus.Models.CheckNameAvailabilityResultAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]</span></span>

### <span data-ttu-id="558c0-123">Пример 1</span><span class="sxs-lookup"><span data-stu-id="558c0-123">Example 1</span></span>
<span data-ttu-id="558c0-124">Сообщение о причине NameAvailable</span><span class="sxs-lookup"><span data-stu-id="558c0-124">NameAvailable Reason Message</span></span>
------------- ------ -------
         True   None

### <span data-ttu-id="558c0-125">Пример 2</span><span class="sxs-lookup"><span data-stu-id="558c0-125">Example 2</span></span>
<span data-ttu-id="558c0-126">Сообщение о причине NameAvailable</span><span class="sxs-lookup"><span data-stu-id="558c0-126">NameAvailable      Reason Message</span></span>
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.

### <span data-ttu-id="558c0-127">Пример 3</span><span class="sxs-lookup"><span data-stu-id="558c0-127">Example 3</span></span>
<span data-ttu-id="558c0-128">Сообщение о причине NameAvailable</span><span class="sxs-lookup"><span data-stu-id="558c0-128">NameAvailable    Reason Message</span></span>
-------------    ------ -------
        False NameInUse The specified service namespace is not available.

## <span data-ttu-id="558c0-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="558c0-129">NOTES</span></span>

## <span data-ttu-id="558c0-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="558c0-130">RELATED LINKS</span></span>
