---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/test-azrelayname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Test-AzRelayName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Test-AzRelayName.md
ms.openlocfilehash: 796f241ebd554647f22e3c5216807e1644c9d769
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904154"
---
# <span data-ttu-id="75c4c-101">Test-AzRelayName</span><span class="sxs-lookup"><span data-stu-id="75c4c-101">Test-AzRelayName</span></span>

## <span data-ttu-id="75c4c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="75c4c-102">SYNOPSIS</span></span>
<span data-ttu-id="75c4c-103">Проверяет доступность указанного имени пространства имен.</span><span class="sxs-lookup"><span data-stu-id="75c4c-103">Checks the Availability of the given NameSpace Name</span></span>

## <span data-ttu-id="75c4c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="75c4c-104">SYNTAX</span></span>

```
Test-AzRelayName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75c4c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="75c4c-105">DESCRIPTION</span></span>
<span data-ttu-id="75c4c-106">Командлет **Test-AzRelayName** проверяет доступность имени пространства имен</span><span class="sxs-lookup"><span data-stu-id="75c4c-106">The **Test-AzRelayName** Cmdlet Check Availability of the NameSpace Name</span></span>

## <span data-ttu-id="75c4c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="75c4c-107">EXAMPLES</span></span>

### <span data-ttu-id="75c4c-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="75c4c-108">Example 1</span></span>
```
PS C:\> Test-AzRelayName -Namespace TestingtheAvailability

NameAvailable Reason Message
------------- ------ -------
         True   None
```

### <span data-ttu-id="75c4c-109">Пример 2</span><span class="sxs-lookup"><span data-stu-id="75c4c-109">Example 2</span></span>
```
PS C:\> Test-AzRelayName -Namespace Testi

NameAvailable      Reason Message
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.
```

### <span data-ttu-id="75c4c-110">Пример 3</span><span class="sxs-lookup"><span data-stu-id="75c4c-110">Example 3</span></span>
```
PS C:\> Test-AzRelayName -Namespace Test123

NameAvailable    Reason Message
-------------    ------ -------
        False NameInUse The specified service namespace is not available.
```

<span data-ttu-id="75c4c-111">Возвращает состояние доступности имени пространства имен.</span><span class="sxs-lookup"><span data-stu-id="75c4c-111">Returns the status on availability of the namespace name</span></span>

## <span data-ttu-id="75c4c-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="75c4c-112">PARAMETERS</span></span>

### <span data-ttu-id="75c4c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75c4c-113">-DefaultProfile</span></span>
<span data-ttu-id="75c4c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="75c4c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75c4c-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="75c4c-115">-Namespace</span></span>
<span data-ttu-id="75c4c-116">Имя пространства имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="75c4c-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="75c4c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75c4c-117">CommonParameters</span></span>
<span data-ttu-id="75c4c-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="75c4c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75c4c-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75c4c-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75c4c-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="75c4c-120">INPUTS</span></span>

### <span data-ttu-id="75c4c-121">System. String</span><span class="sxs-lookup"><span data-stu-id="75c4c-121">System.String</span></span>

## <span data-ttu-id="75c4c-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="75c4c-122">OUTPUTS</span></span>

### <span data-ttu-id="75c4c-123">Microsoft. Azure. Commands. Relay. Models. PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="75c4c-123">Microsoft.Azure.Commands.Relay.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="75c4c-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="75c4c-124">NOTES</span></span>

## <span data-ttu-id="75c4c-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="75c4c-125">RELATED LINKS</span></span>
