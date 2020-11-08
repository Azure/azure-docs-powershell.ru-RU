---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/test-azsignalrname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
ms.openlocfilehash: b00a408df2fe1705309152a02484d3b18ea41e9e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065753"
---
# <span data-ttu-id="7f996-101">Test-AzSignalRName</span><span class="sxs-lookup"><span data-stu-id="7f996-101">Test-AzSignalRName</span></span>

## <span data-ttu-id="7f996-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7f996-102">SYNOPSIS</span></span>
<span data-ttu-id="7f996-103">Проверка доступности имени.</span><span class="sxs-lookup"><span data-stu-id="7f996-103">Check the availability of a name.</span></span> <span data-ttu-id="7f996-104">Alias (псевдоним): Test-AzSignal.</span><span class="sxs-lookup"><span data-stu-id="7f996-104">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="7f996-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7f996-105">SYNTAX</span></span>

```
Test-AzSignalRName [-Name] <String> [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7f996-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7f996-106">DESCRIPTION</span></span>
<span data-ttu-id="7f996-107">Проверка доступности имени.</span><span class="sxs-lookup"><span data-stu-id="7f996-107">Check the availability of a name.</span></span> <span data-ttu-id="7f996-108">Alias (псевдоним): Test-AzSignal.</span><span class="sxs-lookup"><span data-stu-id="7f996-108">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="7f996-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7f996-109">EXAMPLES</span></span>

### <span data-ttu-id="7f996-110">Проверьте существующее имя.</span><span class="sxs-lookup"><span data-stu-id="7f996-110">Check an existed name.</span></span>
```powershell
PS C:\> Test-AzSignalRName -Name existedsignalr -Location eastus
False
```

### <span data-ttu-id="7f996-111">Убедитесь, что имя не существует.</span><span class="sxs-lookup"><span data-stu-id="7f996-111">Check an unexisted name.</span></span>
```
powershell
PS C:\> Test-AzSignalR unexistedsignalr eastus
True
```

## <span data-ttu-id="7f996-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7f996-112">PARAMETERS</span></span>

### <span data-ttu-id="7f996-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f996-113">-DefaultProfile</span></span>
<span data-ttu-id="7f996-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7f996-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f996-115">-Location</span><span class="sxs-lookup"><span data-stu-id="7f996-115">-Location</span></span>
<span data-ttu-id="7f996-116">Расположение службы сигнальных сигналов.</span><span class="sxs-lookup"><span data-stu-id="7f996-116">The SignalR service location.</span></span>

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

### <span data-ttu-id="7f996-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7f996-117">-Name</span></span>
<span data-ttu-id="7f996-118">Название службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="7f996-118">The SignalR service name.</span></span>

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

### <span data-ttu-id="7f996-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f996-119">CommonParameters</span></span>
<span data-ttu-id="7f996-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7f996-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f996-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7f996-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f996-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7f996-122">INPUTS</span></span>

### <span data-ttu-id="7f996-123">System. String</span><span class="sxs-lookup"><span data-stu-id="7f996-123">System.String</span></span>

## <span data-ttu-id="7f996-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7f996-124">OUTPUTS</span></span>

### <span data-ttu-id="7f996-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7f996-125">System.Boolean</span></span>

## <span data-ttu-id="7f996-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="7f996-126">NOTES</span></span>

## <span data-ttu-id="7f996-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7f996-127">RELATED LINKS</span></span>
