---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/test-azurermrelayname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
ms.openlocfilehash: adf7c4b7f8d80e16b49d9d55b742a55279232a07
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566139"
---
# <span data-ttu-id="3247f-101">Test-AzureRmRelayName</span><span class="sxs-lookup"><span data-stu-id="3247f-101">Test-AzureRmRelayName</span></span>

## <span data-ttu-id="3247f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3247f-102">SYNOPSIS</span></span>
<span data-ttu-id="3247f-103">Проверяет доступность указанного имени пространства имен.</span><span class="sxs-lookup"><span data-stu-id="3247f-103">Checks the Availability of the given NameSpace Name</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3247f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3247f-104">SYNTAX</span></span>

```
Test-AzureRmRelayName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3247f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3247f-105">DESCRIPTION</span></span>
<span data-ttu-id="3247f-106">Командлет **Test-AzureRmRelayName** проверяет доступность имени пространства имен</span><span class="sxs-lookup"><span data-stu-id="3247f-106">The **Test-AzureRmRelayName** Cmdlet Check Availability of the NameSpace Name</span></span>

## <span data-ttu-id="3247f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3247f-107">EXAMPLES</span></span>

### <span data-ttu-id="3247f-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3247f-108">Example 1</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace TestingtheAvailability
```

### <span data-ttu-id="3247f-109">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3247f-109">Example 2</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace Testi
```

### <span data-ttu-id="3247f-110">Пример 3</span><span class="sxs-lookup"><span data-stu-id="3247f-110">Example 3</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace Test123
```

<span data-ttu-id="3247f-111">Возвращает состояние доступности имени пространства имен.</span><span class="sxs-lookup"><span data-stu-id="3247f-111">Returns the status on availability of the namespace name</span></span>

## <span data-ttu-id="3247f-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3247f-112">PARAMETERS</span></span>

### <span data-ttu-id="3247f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3247f-113">-DefaultProfile</span></span>
<span data-ttu-id="3247f-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3247f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3247f-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3247f-115">-Namespace</span></span>
<span data-ttu-id="3247f-116">Имя пространства имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="3247f-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="3247f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3247f-117">CommonParameters</span></span>
<span data-ttu-id="3247f-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3247f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3247f-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3247f-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3247f-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3247f-120">INPUTS</span></span>

### <span data-ttu-id="3247f-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3247f-121">-Namespace</span></span>
 <span data-ttu-id="3247f-122">System. String</span><span class="sxs-lookup"><span data-stu-id="3247f-122">System.String</span></span>

## <span data-ttu-id="3247f-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3247f-123">OUTPUTS</span></span>

### <span data-ttu-id="3247f-124">[Microsoft. Azure. Commands. Relay. Models. CheckNameAvailabilityResultAttributes, Microsoft. Azure. Commands. Relay, Version = 0.1.0.0, культура = Neutral, PublicKeyToken = NULL]</span><span class="sxs-lookup"><span data-stu-id="3247f-124">[Microsoft.Azure.Commands.Relay.Models.CheckNameAvailabilityResultAttributes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]</span></span>

### <span data-ttu-id="3247f-125">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3247f-125">Example 1</span></span>
<span data-ttu-id="3247f-126">Сообщение о причине NameAvailable</span><span class="sxs-lookup"><span data-stu-id="3247f-126">NameAvailable Reason Message</span></span>
------------- ------ -------
         True   None

### <span data-ttu-id="3247f-127">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3247f-127">Example 2</span></span>
<span data-ttu-id="3247f-128">Сообщение о причине NameAvailable</span><span class="sxs-lookup"><span data-stu-id="3247f-128">NameAvailable      Reason Message</span></span>
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.

### <span data-ttu-id="3247f-129">Пример 3</span><span class="sxs-lookup"><span data-stu-id="3247f-129">Example 3</span></span>
<span data-ttu-id="3247f-130">Сообщение о причине NameAvailable</span><span class="sxs-lookup"><span data-stu-id="3247f-130">NameAvailable    Reason Message</span></span>
-------------    ------ -------
        False NameInUse The specified service namespace is not available.

## <span data-ttu-id="3247f-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="3247f-131">NOTES</span></span>

## <span data-ttu-id="3247f-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3247f-132">RELATED LINKS</span></span>

