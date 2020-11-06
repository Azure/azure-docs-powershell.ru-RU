---
external help file: AzureRM.Compute.ManagedService-help.xml
Module Name: AzureRM.Compute.ManagedService
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute.managedservice/convertto-azurermvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute.ManagedService/Commands.Compute.ManagedService/help/ConvertTo-AzureRmVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute.ManagedService/Commands.Compute.ManagedService/help/ConvertTo-AzureRmVhd.md
ms.openlocfilehash: 0fa0f2d5cb78fe96f05b818b5cbfdabca47cbdee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558491"
---
# <span data-ttu-id="c6e6a-101">ConvertTo-AzureRmVhd</span><span class="sxs-lookup"><span data-stu-id="c6e6a-101">ConvertTo-AzureRmVhd</span></span>

## <span data-ttu-id="c6e6a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c6e6a-102">SYNOPSIS</span></span>
<span data-ttu-id="c6e6a-103">Преобразование виртуальной машины Hyper-V в Azure файлы виртуальных жестких дисков поддерживаются</span><span class="sxs-lookup"><span data-stu-id="c6e6a-103">Convert Hyper-V VM to Azure supported virtual hard disk files</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6e6a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c6e6a-104">SYNTAX</span></span>

```
ConvertTo-AzureRmVhd -HyperVVMName <String> -ExportPath <String> [-HyperVServer <String>] [-Force] [-AsJob]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6e6a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c6e6a-105">DESCRIPTION</span></span>
<span data-ttu-id="c6e6a-106">Преобразование виртуальной машины Hyper-V в Azure файлы виртуальных жестких дисков поддерживаются</span><span class="sxs-lookup"><span data-stu-id="c6e6a-106">Convert Hyper-V VM to Azure supported virtual hard disk files</span></span>

## <span data-ttu-id="c6e6a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c6e6a-107">EXAMPLES</span></span>

### <span data-ttu-id="c6e6a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c6e6a-108">Example 1</span></span>
```
PS C:\> ConvertTo-AzureRmVhd -HyperVVMName 'test' -ExportPath '.';
.\test\Virtual Hard Disks\Converted\os.vhd
.\test\Virtual Hard Disks\Converted\disk.vhd
```

<span data-ttu-id="c6e6a-109">Преобразование виртуальной машины Hyper-V с именем "тест" в службу Azure Поддерживаемые виртуальные жесткие диски в текущую папку.</span><span class="sxs-lookup"><span data-stu-id="c6e6a-109">Convert Hyper-V VM named 'test' to Azure supported virtual hard disk files to the current folder.</span></span>

## <span data-ttu-id="c6e6a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c6e6a-110">PARAMETERS</span></span>

### <span data-ttu-id="c6e6a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c6e6a-111">-AsJob</span></span>
<span data-ttu-id="c6e6a-112">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="c6e6a-112">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6e6a-113">-ExportPath</span><span class="sxs-lookup"><span data-stu-id="c6e6a-113">-ExportPath</span></span>
<span data-ttu-id="c6e6a-114">Путь к папке для экспорта, в которой будут храниться файлы на диске.</span><span class="sxs-lookup"><span data-stu-id="c6e6a-114">The export folder path that will contain the disk files.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6e6a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c6e6a-115">-Force</span></span>
<span data-ttu-id="c6e6a-116">Принудительно выполнить экспорт, даже если найдена существующая папка.</span><span class="sxs-lookup"><span data-stu-id="c6e6a-116">Force the export even if existing folder is found.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6e6a-117">-HyperVServer</span><span class="sxs-lookup"><span data-stu-id="c6e6a-117">-HyperVServer</span></span>
<span data-ttu-id="c6e6a-118">DNS-имя сервера Hyper-V, в качестве значения по умолчанию — "localhost".</span><span class="sxs-lookup"><span data-stu-id="c6e6a-118">The Hyper-V server DNS name, with 'localhost' as the default value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Localhost
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6e6a-119">-HyperVVMName</span><span class="sxs-lookup"><span data-stu-id="c6e6a-119">-HyperVVMName</span></span>
<span data-ttu-id="c6e6a-120">Имя Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="c6e6a-120">The Hyper-V name name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6e6a-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c6e6a-121">-Confirm</span></span>
<span data-ttu-id="c6e6a-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c6e6a-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6e6a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6e6a-123">-WhatIf</span></span>
<span data-ttu-id="c6e6a-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c6e6a-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c6e6a-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c6e6a-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6e6a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6e6a-126">CommonParameters</span></span>
<span data-ttu-id="c6e6a-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c6e6a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6e6a-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6e6a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6e6a-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c6e6a-129">INPUTS</span></span>

### <span data-ttu-id="c6e6a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c6e6a-130">System.String</span></span>

## <span data-ttu-id="c6e6a-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c6e6a-131">OUTPUTS</span></span>

### <span data-ttu-id="c6e6a-132">System. Management. Automation. PathInfo</span><span class="sxs-lookup"><span data-stu-id="c6e6a-132">System.Management.Automation.PathInfo</span></span>

## <span data-ttu-id="c6e6a-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="c6e6a-133">NOTES</span></span>

## <span data-ttu-id="c6e6a-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c6e6a-134">RELATED LINKS</span></span>
