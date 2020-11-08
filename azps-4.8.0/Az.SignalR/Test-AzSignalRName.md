---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/test-azsignalrname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
ms.openlocfilehash: b00a408df2fe1705309152a02484d3b18ea41e9e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235319"
---
# <span data-ttu-id="5e564-101">Test-AzSignalRName</span><span class="sxs-lookup"><span data-stu-id="5e564-101">Test-AzSignalRName</span></span>

## <span data-ttu-id="5e564-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5e564-102">SYNOPSIS</span></span>
<span data-ttu-id="5e564-103">Проверка доступности имени.</span><span class="sxs-lookup"><span data-stu-id="5e564-103">Check the availability of a name.</span></span> <span data-ttu-id="5e564-104">Alias (псевдоним): Test-AzSignal.</span><span class="sxs-lookup"><span data-stu-id="5e564-104">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="5e564-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5e564-105">SYNTAX</span></span>

```
Test-AzSignalRName [-Name] <String> [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5e564-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5e564-106">DESCRIPTION</span></span>
<span data-ttu-id="5e564-107">Проверка доступности имени.</span><span class="sxs-lookup"><span data-stu-id="5e564-107">Check the availability of a name.</span></span> <span data-ttu-id="5e564-108">Alias (псевдоним): Test-AzSignal.</span><span class="sxs-lookup"><span data-stu-id="5e564-108">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="5e564-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5e564-109">EXAMPLES</span></span>

### <span data-ttu-id="5e564-110">Проверьте существующее имя.</span><span class="sxs-lookup"><span data-stu-id="5e564-110">Check an existed name.</span></span>
```powershell
PS C:\> Test-AzSignalRName -Name existedsignalr -Location eastus
False
```

### <span data-ttu-id="5e564-111">Убедитесь, что имя не существует.</span><span class="sxs-lookup"><span data-stu-id="5e564-111">Check an unexisted name.</span></span>
```
powershell
PS C:\> Test-AzSignalR unexistedsignalr eastus
True
```

## <span data-ttu-id="5e564-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5e564-112">PARAMETERS</span></span>

### <span data-ttu-id="5e564-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e564-113">-DefaultProfile</span></span>
<span data-ttu-id="5e564-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5e564-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e564-115">-Location</span><span class="sxs-lookup"><span data-stu-id="5e564-115">-Location</span></span>
<span data-ttu-id="5e564-116">Расположение службы сигнальных сигналов.</span><span class="sxs-lookup"><span data-stu-id="5e564-116">The SignalR service location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e564-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5e564-117">-Name</span></span>
<span data-ttu-id="5e564-118">Название службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="5e564-118">The SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e564-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e564-119">CommonParameters</span></span>
<span data-ttu-id="5e564-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5e564-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e564-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e564-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e564-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5e564-122">INPUTS</span></span>

### <span data-ttu-id="5e564-123">System. String</span><span class="sxs-lookup"><span data-stu-id="5e564-123">System.String</span></span>

## <span data-ttu-id="5e564-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5e564-124">OUTPUTS</span></span>

### <span data-ttu-id="5e564-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5e564-125">System.Boolean</span></span>

## <span data-ttu-id="5e564-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="5e564-126">NOTES</span></span>

## <span data-ttu-id="5e564-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5e564-127">RELATED LINKS</span></span>