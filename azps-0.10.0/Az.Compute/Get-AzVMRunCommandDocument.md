---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmruncommanddocument
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
ms.openlocfilehash: 45d051e5fc2fe750f58dc6400a037960b7eb9c7c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911512"
---
# <span data-ttu-id="b9242-101">Get-AzVMRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="b9242-101">Get-AzVMRunCommandDocument</span></span>

## <span data-ttu-id="b9242-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b9242-102">SYNOPSIS</span></span>
<span data-ttu-id="b9242-103">Открыть командный документ.</span><span class="sxs-lookup"><span data-stu-id="b9242-103">Get run command document.</span></span>

## <span data-ttu-id="b9242-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b9242-104">SYNTAX</span></span>

```
Get-AzVMRunCommandDocument [-Location] <String> [[-CommandId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9242-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9242-105">DESCRIPTION</span></span>
<span data-ttu-id="b9242-106">Открыть командный документ.</span><span class="sxs-lookup"><span data-stu-id="b9242-106">Get run command document.</span></span>

## <span data-ttu-id="b9242-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b9242-107">EXAMPLES</span></span>

### <span data-ttu-id="b9242-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b9242-108">Example 1</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus' -CommandId 'RunPowerShellScript'
```

<span data-ttu-id="b9242-109">Возвращает определенный документ команды запуска для "RunPowerShellScript" в "westus".</span><span class="sxs-lookup"><span data-stu-id="b9242-109">Gets a specific run command document for 'RunPowerShellScript' in 'westus'.</span></span>


<span data-ttu-id="b9242-110">$Loc расположения Get-AzVMRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="b9242-110">Get-AzVMRunCommandDocument -Location $loc</span></span>

### <span data-ttu-id="b9242-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b9242-111">Example 2</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus'
```

<span data-ttu-id="b9242-112">Список всех доступных команд выполнения в "westus".</span><span class="sxs-lookup"><span data-stu-id="b9242-112">Lists all available run commands in 'westus'.</span></span>

## <span data-ttu-id="b9242-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b9242-113">PARAMETERS</span></span>

### <span data-ttu-id="b9242-114">-CommandId</span><span class="sxs-lookup"><span data-stu-id="b9242-114">-CommandId</span></span>
<span data-ttu-id="b9242-115">Идентификатор команды.</span><span class="sxs-lookup"><span data-stu-id="b9242-115">The command id.</span></span>

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

### <span data-ttu-id="b9242-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9242-116">-DefaultProfile</span></span>
<span data-ttu-id="b9242-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b9242-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9242-118">-Location</span><span class="sxs-lookup"><span data-stu-id="b9242-118">-Location</span></span>
<span data-ttu-id="b9242-119">Расположение, в котором запрашиваются команды выполнения.</span><span class="sxs-lookup"><span data-stu-id="b9242-119">The location upon which run commands is queried.</span></span>

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

### <span data-ttu-id="b9242-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9242-120">CommonParameters</span></span>
<span data-ttu-id="b9242-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b9242-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9242-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9242-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9242-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b9242-123">INPUTS</span></span>

### <span data-ttu-id="b9242-124">System. String</span><span class="sxs-lookup"><span data-stu-id="b9242-124">System.String</span></span>

## <span data-ttu-id="b9242-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9242-125">OUTPUTS</span></span>

### <span data-ttu-id="b9242-126">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="b9242-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span></span>

## <span data-ttu-id="b9242-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="b9242-127">NOTES</span></span>

## <span data-ttu-id="b9242-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b9242-128">RELATED LINKS</span></span>

