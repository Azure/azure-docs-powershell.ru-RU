---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/test-azrelayname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Test-AzRelayName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Test-AzRelayName.md
ms.openlocfilehash: 45c3e0a4271a5eb2527ff25b5858a3f5aa35dc0a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94315752"
---
# <span data-ttu-id="c37fe-101">Test-AzRelayName</span><span class="sxs-lookup"><span data-stu-id="c37fe-101">Test-AzRelayName</span></span>

## <span data-ttu-id="c37fe-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c37fe-102">SYNOPSIS</span></span>
<span data-ttu-id="c37fe-103">Проверяет доступность указанного имени пространства имен.</span><span class="sxs-lookup"><span data-stu-id="c37fe-103">Checks the Availability of the given NameSpace Name</span></span>

## <span data-ttu-id="c37fe-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c37fe-104">SYNTAX</span></span>

```
Test-AzRelayName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c37fe-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c37fe-105">DESCRIPTION</span></span>
<span data-ttu-id="c37fe-106">Командлет **Test-AzRelayName** проверяет доступность имени пространства имен</span><span class="sxs-lookup"><span data-stu-id="c37fe-106">The **Test-AzRelayName** Cmdlet Check Availability of the NameSpace Name</span></span>

## <span data-ttu-id="c37fe-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c37fe-107">EXAMPLES</span></span>

### <span data-ttu-id="c37fe-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c37fe-108">Example 1</span></span>
```
PS C:\> Test-AzRelayName -Namespace TestingtheAvailability

NameAvailable Reason Message
------------- ------ -------
         True   None
```

### <span data-ttu-id="c37fe-109">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c37fe-109">Example 2</span></span>
```
PS C:\> Test-AzRelayName -Namespace Testi

NameAvailable      Reason Message
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.
```

### <span data-ttu-id="c37fe-110">Пример 3</span><span class="sxs-lookup"><span data-stu-id="c37fe-110">Example 3</span></span>
```
PS C:\> Test-AzRelayName -Namespace Test123

NameAvailable    Reason Message
-------------    ------ -------
        False NameInUse The specified service namespace is not available.
```

<span data-ttu-id="c37fe-111">Возвращает состояние доступности имени пространства имен.</span><span class="sxs-lookup"><span data-stu-id="c37fe-111">Returns the status on availability of the namespace name</span></span>

## <span data-ttu-id="c37fe-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c37fe-112">PARAMETERS</span></span>

### <span data-ttu-id="c37fe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c37fe-113">-DefaultProfile</span></span>
<span data-ttu-id="c37fe-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c37fe-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c37fe-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c37fe-115">-Namespace</span></span>
<span data-ttu-id="c37fe-116">Имя пространства имен ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="c37fe-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="c37fe-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c37fe-117">CommonParameters</span></span>
<span data-ttu-id="c37fe-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c37fe-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c37fe-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c37fe-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c37fe-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c37fe-120">INPUTS</span></span>

### <span data-ttu-id="c37fe-121">System. String</span><span class="sxs-lookup"><span data-stu-id="c37fe-121">System.String</span></span>

## <span data-ttu-id="c37fe-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c37fe-122">OUTPUTS</span></span>

### <span data-ttu-id="c37fe-123">Microsoft. Azure. Commands. Relay. Models. PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="c37fe-123">Microsoft.Azure.Commands.Relay.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="c37fe-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="c37fe-124">NOTES</span></span>

## <span data-ttu-id="c37fe-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c37fe-125">RELATED LINKS</span></span>
