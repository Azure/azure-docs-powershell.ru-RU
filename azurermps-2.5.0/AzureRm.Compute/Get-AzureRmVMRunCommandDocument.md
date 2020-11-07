---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmruncommanddocument
schema: 2.0.0
ms.openlocfilehash: d51528cab51e4e6fe6cda428e25965d65c449c4b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914610"
---
# <span data-ttu-id="6d8c6-101">Get-AzureRmVMRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="6d8c6-101">Get-AzureRmVMRunCommandDocument</span></span>

## <span data-ttu-id="6d8c6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6d8c6-102">SYNOPSIS</span></span>
<span data-ttu-id="6d8c6-103">Открыть командный документ.</span><span class="sxs-lookup"><span data-stu-id="6d8c6-103">Get run command document.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d8c6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6d8c6-104">SYNTAX</span></span>

```
Get-AzureRmVMRunCommandDocument [-Location] <String> [[-CommandId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d8c6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d8c6-105">DESCRIPTION</span></span>
<span data-ttu-id="6d8c6-106">Открыть командный документ.</span><span class="sxs-lookup"><span data-stu-id="6d8c6-106">Get run command document.</span></span>

## <span data-ttu-id="6d8c6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6d8c6-107">EXAMPLES</span></span>

### <span data-ttu-id="6d8c6-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6d8c6-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVMRunCommandDocument -Location 'westus' -CommandId 'RunPowerShellScript'
```

<span data-ttu-id="6d8c6-109">Возвращает определенный документ команды запуска для "RunPowerShellScript" в "westus".</span><span class="sxs-lookup"><span data-stu-id="6d8c6-109">Gets a specific run command document for 'RunPowerShellScript' in 'westus'.</span></span>


<span data-ttu-id="6d8c6-110">$Loc расположения Get-AzureRmVMRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="6d8c6-110">Get-AzureRmVMRunCommandDocument -Location $loc</span></span>

### <span data-ttu-id="6d8c6-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6d8c6-111">Example 2</span></span>
```
PS C:\> Get-AzureRmVMRunCommandDocument -Location 'westus'
```

<span data-ttu-id="6d8c6-112">Список всех доступных команд выполнения в "westus".</span><span class="sxs-lookup"><span data-stu-id="6d8c6-112">Lists all available run commands in 'westus'.</span></span>

## <span data-ttu-id="6d8c6-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6d8c6-113">PARAMETERS</span></span>

### <span data-ttu-id="6d8c6-114">-CommandId</span><span class="sxs-lookup"><span data-stu-id="6d8c6-114">-CommandId</span></span>
<span data-ttu-id="6d8c6-115">Идентификатор команды.</span><span class="sxs-lookup"><span data-stu-id="6d8c6-115">The command id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d8c6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d8c6-116">-DefaultProfile</span></span>
<span data-ttu-id="6d8c6-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6d8c6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d8c6-118">-Location</span><span class="sxs-lookup"><span data-stu-id="6d8c6-118">-Location</span></span>
<span data-ttu-id="6d8c6-119">Расположение, в котором запрашиваются команды выполнения.</span><span class="sxs-lookup"><span data-stu-id="6d8c6-119">The location upon which run commands is queried.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d8c6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d8c6-120">CommonParameters</span></span>
<span data-ttu-id="6d8c6-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6d8c6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d8c6-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d8c6-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d8c6-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6d8c6-123">INPUTS</span></span>

### <span data-ttu-id="6d8c6-124">System. String</span><span class="sxs-lookup"><span data-stu-id="6d8c6-124">System.String</span></span>

## <span data-ttu-id="6d8c6-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d8c6-125">OUTPUTS</span></span>

### <span data-ttu-id="6d8c6-126">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="6d8c6-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span></span>

## <span data-ttu-id="6d8c6-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="6d8c6-127">NOTES</span></span>

## <span data-ttu-id="6d8c6-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6d8c6-128">RELATED LINKS</span></span>

