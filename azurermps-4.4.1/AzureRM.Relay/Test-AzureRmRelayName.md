---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
ms.openlocfilehash: 4b3afc0b41f6eaf68e7ec0c4f8ed976b36267c97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559555"
---
# <span data-ttu-id="44585-101">Test-AzureRmRelayName</span><span class="sxs-lookup"><span data-stu-id="44585-101">Test-AzureRmRelayName</span></span>

## <span data-ttu-id="44585-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="44585-102">SYNOPSIS</span></span>
<span data-ttu-id="44585-103">Проверяет доступность указанного имени пространства имен.</span><span class="sxs-lookup"><span data-stu-id="44585-103">Checks the Availability of the given NameSpace Name</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44585-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="44585-104">SYNTAX</span></span>

```
Test-AzureRmRelayName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44585-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="44585-105">DESCRIPTION</span></span>
<span data-ttu-id="44585-106">Командлет **Test-AzureRmRelayName** проверяет доступность имени пространства имен</span><span class="sxs-lookup"><span data-stu-id="44585-106">The **Test-AzureRmRelayName** Cmdlet Check Availability of the NameSpace Name</span></span>

## <span data-ttu-id="44585-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="44585-107">EXAMPLES</span></span>

### <span data-ttu-id="44585-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="44585-108">Example 1</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace TestingtheAvailability
```

### <span data-ttu-id="44585-109">Пример 2</span><span class="sxs-lookup"><span data-stu-id="44585-109">Example 2</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace Testi
```

### <span data-ttu-id="44585-110">Пример 3</span><span class="sxs-lookup"><span data-stu-id="44585-110">Example 3</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace Test123
```

<span data-ttu-id="44585-111">Возвращает состояние доступности имени пространства имен.</span><span class="sxs-lookup"><span data-stu-id="44585-111">Returns the status on availability of the namespace name</span></span>

## <span data-ttu-id="44585-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="44585-112">PARAMETERS</span></span>

### <span data-ttu-id="44585-113">-Namespace</span><span class="sxs-lookup"><span data-stu-id="44585-113">-Namespace</span></span>
<span data-ttu-id="44585-114">Имя пространства имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="44585-114">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="44585-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44585-115">-DefaultProfile</span></span>
<span data-ttu-id="44585-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="44585-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44585-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44585-117">CommonParameters</span></span>
<span data-ttu-id="44585-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="44585-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44585-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44585-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44585-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="44585-120">INPUTS</span></span>

### <span data-ttu-id="44585-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="44585-121">-Namespace</span></span>
 <span data-ttu-id="44585-122">System. String</span><span class="sxs-lookup"><span data-stu-id="44585-122">System.String</span></span>

## <span data-ttu-id="44585-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="44585-123">OUTPUTS</span></span>

### <span data-ttu-id="44585-124">[Microsoft. Azure. Commands. Relay. Models. CheckNameAvailabilityResultAttributes, Microsoft. Azure. Commands. Relay, Version = 0.1.0.0, культура = Neutral, PublicKeyToken = NULL]</span><span class="sxs-lookup"><span data-stu-id="44585-124">[Microsoft.Azure.Commands.Relay.Models.CheckNameAvailabilityResultAttributes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]</span></span>

### <span data-ttu-id="44585-125">Пример 1</span><span class="sxs-lookup"><span data-stu-id="44585-125">Example 1</span></span>
<span data-ttu-id="44585-126">Сообщение о причине NameAvailable</span><span class="sxs-lookup"><span data-stu-id="44585-126">NameAvailable Reason Message</span></span>
------------- ------ -------
         True   None

### <span data-ttu-id="44585-127">Пример 2</span><span class="sxs-lookup"><span data-stu-id="44585-127">Example 2</span></span>
<span data-ttu-id="44585-128">Сообщение о причине NameAvailable</span><span class="sxs-lookup"><span data-stu-id="44585-128">NameAvailable      Reason Message</span></span>
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.

### <span data-ttu-id="44585-129">Пример 3</span><span class="sxs-lookup"><span data-stu-id="44585-129">Example 3</span></span>
<span data-ttu-id="44585-130">Сообщение о причине NameAvailable</span><span class="sxs-lookup"><span data-stu-id="44585-130">NameAvailable    Reason Message</span></span>
-------------    ------ -------
        False NameInUse The specified service namespace is not available.

## <span data-ttu-id="44585-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="44585-131">NOTES</span></span>

## <span data-ttu-id="44585-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="44585-132">RELATED LINKS</span></span>

