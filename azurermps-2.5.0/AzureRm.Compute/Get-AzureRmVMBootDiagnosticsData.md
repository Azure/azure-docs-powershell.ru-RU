---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 15CAC050-F2E9-4872-88E7-516A6D194FAB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmbootdiagnosticsdata
schema: 2.0.0
ms.openlocfilehash: 867f2c14e90eddd9649e0720d41f56aa896c61ff
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913674"
---
# <span data-ttu-id="6e082-101">Get-AzureRmVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="6e082-101">Get-AzureRmVMBootDiagnosticsData</span></span>

## <span data-ttu-id="6e082-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6e082-102">SYNOPSIS</span></span>
<span data-ttu-id="6e082-103">Получение данных диагностики загрузки для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6e082-103">Gets boot diagnostics data for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e082-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6e082-104">SYNTAX</span></span>

### <span data-ttu-id="6e082-105">WindowsParamSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6e082-105">WindowsParamSet (Default)</span></span>
```
Get-AzureRmVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Windows]
 [-LocalPath] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e082-106">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="6e082-106">LinuxParamSet</span></span>
```
Get-AzureRmVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Linux]
 [[-LocalPath] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e082-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6e082-107">DESCRIPTION</span></span>
<span data-ttu-id="6e082-108">Командлет **Get-AzureRmVMBootDiagnosticsData** получает данные диагностики загрузки для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6e082-108">The **Get-AzureRmVMBootDiagnosticsData** cmdlet gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="6e082-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6e082-109">EXAMPLES</span></span>

### <span data-ttu-id="6e082-110">Пример 1: получение данных диагностики загрузки</span><span class="sxs-lookup"><span data-stu-id="6e082-110">Example 1: Get boot diagnostics data</span></span>
```
PS C:\> Get-AzureRmVMBootDiagnosticsData -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07" -Windows -LocalPath "C:\Contoso\BootDiagnostics"
```

<span data-ttu-id="6e082-111">Эта команда возвращает данные диагностики загрузки для виртуальной машины с именем ContosoVM07.</span><span class="sxs-lookup"><span data-stu-id="6e082-111">This command gets boot diagnostics data for the virtual machine named ContosoVM07.</span></span>
<span data-ttu-id="6e082-112">Эта виртуальная машина запускает операционную систему Windows.</span><span class="sxs-lookup"><span data-stu-id="6e082-112">This virtual machine runs the Windows operating system.</span></span>
<span data-ttu-id="6e082-113">Команда сохраняет данные в указанном локальном пути.</span><span class="sxs-lookup"><span data-stu-id="6e082-113">The command stores the data in specified local path.</span></span>

## <span data-ttu-id="6e082-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6e082-114">PARAMETERS</span></span>

### <span data-ttu-id="6e082-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e082-115">-DefaultProfile</span></span>
<span data-ttu-id="6e082-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6e082-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6e082-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="6e082-117">-Linux</span></span>
<span data-ttu-id="6e082-118">Указывает на то, что виртуальная машина работает под управлением операционной системы Linux.</span><span class="sxs-lookup"><span data-stu-id="6e082-118">Indicates that the virtual machine runs the Linux operating system.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LinuxParamSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e082-119">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="6e082-119">-LocalPath</span></span>
<span data-ttu-id="6e082-120">Указывает локальный путь для данных диагностики загрузки.</span><span class="sxs-lookup"><span data-stu-id="6e082-120">Specifies the local path for the boot diagnostics data.</span></span>

```yaml
Type: String
Parameter Sets: WindowsParamSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: LinuxParamSet
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e082-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6e082-121">-Name</span></span>
<span data-ttu-id="6e082-122">Указывает имя виртуальной машины, для которой этот командлет получает данные диагностики.</span><span class="sxs-lookup"><span data-stu-id="6e082-122">Specifies the name of the virtual machine for which this cmdlet gets diagnostics data.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e082-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e082-123">-ResourceGroupName</span></span>
<span data-ttu-id="6e082-124">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6e082-124">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="6e082-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="6e082-125">-Windows</span></span>
<span data-ttu-id="6e082-126">Указывает на то, что виртуальная машина работает под управлением операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="6e082-126">Indicates that the virtual machine runs the Windows operating system.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WindowsParamSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e082-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e082-127">CommonParameters</span></span>
<span data-ttu-id="6e082-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6e082-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e082-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e082-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e082-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6e082-130">INPUTS</span></span>

### <span data-ttu-id="6e082-131">Ничего</span><span class="sxs-lookup"><span data-stu-id="6e082-131">None</span></span>
<span data-ttu-id="6e082-132">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="6e082-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6e082-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6e082-133">OUTPUTS</span></span>

### <span data-ttu-id="6e082-134">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="6e082-134">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="6e082-135">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="6e082-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="6e082-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="6e082-136">NOTES</span></span>

## <span data-ttu-id="6e082-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6e082-137">RELATED LINKS</span></span>

[<span data-ttu-id="6e082-138">Set-AzureRmVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="6e082-138">Set-AzureRmVMBootDiagnostics</span></span>](./Set-AzureRmVMBootDiagnostics.md)


