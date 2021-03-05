---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/test-azrelayname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Test-AzRelayName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Test-AzRelayName.md
ms.openlocfilehash: be0b0f2aa9aa45fa69b3d57051a5671a76186abc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000339"
---
# <span data-ttu-id="5eb40-101">Test-AzRelayName</span><span class="sxs-lookup"><span data-stu-id="5eb40-101">Test-AzRelayName</span></span>

## <span data-ttu-id="5eb40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5eb40-102">SYNOPSIS</span></span>
<span data-ttu-id="5eb40-103">Проверка доступности заданного имени пространства имен</span><span class="sxs-lookup"><span data-stu-id="5eb40-103">Checks the Availability of the given NameSpace Name</span></span>

## <span data-ttu-id="5eb40-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5eb40-104">SYNTAX</span></span>

```
Test-AzRelayName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5eb40-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5eb40-105">DESCRIPTION</span></span>
<span data-ttu-id="5eb40-106">Проверка доступности имени пространства имен для проверки доступности для **test-AzRelayName**</span><span class="sxs-lookup"><span data-stu-id="5eb40-106">The **Test-AzRelayName** Cmdlet Check Availability of the NameSpace Name</span></span>

## <span data-ttu-id="5eb40-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5eb40-107">EXAMPLES</span></span>

### <span data-ttu-id="5eb40-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5eb40-108">Example 1</span></span>
```
PS C:\> Test-AzRelayName -Namespace TestingtheAvailability

NameAvailable Reason Message
------------- ------ -------
         True   None
```

### <span data-ttu-id="5eb40-109">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5eb40-109">Example 2</span></span>
```
PS C:\> Test-AzRelayName -Namespace Testi

NameAvailable      Reason Message
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.
```

### <span data-ttu-id="5eb40-110">Пример 3</span><span class="sxs-lookup"><span data-stu-id="5eb40-110">Example 3</span></span>
```
PS C:\> Test-AzRelayName -Namespace Test123

NameAvailable    Reason Message
-------------    ------ -------
        False NameInUse The specified service namespace is not available.
```

<span data-ttu-id="5eb40-111">Возвращает состояние доступности имени пространства имен.</span><span class="sxs-lookup"><span data-stu-id="5eb40-111">Returns the status on availability of the namespace name</span></span>

## <span data-ttu-id="5eb40-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5eb40-112">PARAMETERS</span></span>

### <span data-ttu-id="5eb40-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5eb40-113">-DefaultProfile</span></span>
<span data-ttu-id="5eb40-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5eb40-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5eb40-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5eb40-115">-Namespace</span></span>
<span data-ttu-id="5eb40-116">Имя пространства ретрансляции.</span><span class="sxs-lookup"><span data-stu-id="5eb40-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="5eb40-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5eb40-117">CommonParameters</span></span>
<span data-ttu-id="5eb40-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5eb40-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5eb40-119">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5eb40-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5eb40-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5eb40-120">INPUTS</span></span>

### <span data-ttu-id="5eb40-121">System.String</span><span class="sxs-lookup"><span data-stu-id="5eb40-121">System.String</span></span>

## <span data-ttu-id="5eb40-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5eb40-122">OUTPUTS</span></span>

### <span data-ttu-id="5eb40-123">Microsoft.Azure.Commands.Relay.Models.PSCheckNameAvailabilityResultAttributes</span><span class="sxs-lookup"><span data-stu-id="5eb40-123">Microsoft.Azure.Commands.Relay.Models.PSCheckNameAvailabilityResultAttributes</span></span>

## <span data-ttu-id="5eb40-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5eb40-124">NOTES</span></span>

## <span data-ttu-id="5eb40-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5eb40-125">RELATED LINKS</span></span>
