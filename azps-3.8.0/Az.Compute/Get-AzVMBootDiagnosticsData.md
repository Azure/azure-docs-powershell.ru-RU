---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 15CAC050-F2E9-4872-88E7-516A6D194FAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmbootdiagnosticsdata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMBootDiagnosticsData.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMBootDiagnosticsData.md
ms.openlocfilehash: c56c9e586b0089311477fc12b6624c74321f9a0b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94075057"
---
# <span data-ttu-id="c5212-101">Get-AzVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="c5212-101">Get-AzVMBootDiagnosticsData</span></span>

## <span data-ttu-id="c5212-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c5212-102">SYNOPSIS</span></span>
<span data-ttu-id="c5212-103">Получение данных диагностики загрузки для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c5212-103">Gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="c5212-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c5212-104">SYNTAX</span></span>

### <span data-ttu-id="c5212-105">WindowsParamSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c5212-105">WindowsParamSet (Default)</span></span>
```
Get-AzVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Windows] [-LocalPath] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5212-106">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="c5212-106">LinuxParamSet</span></span>
```
Get-AzVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Linux] [[-LocalPath] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5212-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c5212-107">DESCRIPTION</span></span>
<span data-ttu-id="c5212-108">Командлет **Get-AzVMBootDiagnosticsData** получает данные диагностики загрузки для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c5212-108">The **Get-AzVMBootDiagnosticsData** cmdlet gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="c5212-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c5212-109">EXAMPLES</span></span>

### <span data-ttu-id="c5212-110">Пример 1: получение данных диагностики загрузки</span><span class="sxs-lookup"><span data-stu-id="c5212-110">Example 1: Get boot diagnostics data</span></span>
```
PS C:\> Get-AzVMBootDiagnosticsData -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07" -Windows -LocalPath "C:\Contoso\BootDiagnostics"
```

<span data-ttu-id="c5212-111">Эта команда возвращает данные диагностики загрузки для виртуальной машины с именем ContosoVM07.</span><span class="sxs-lookup"><span data-stu-id="c5212-111">This command gets boot diagnostics data for the virtual machine named ContosoVM07.</span></span>
<span data-ttu-id="c5212-112">Эта виртуальная машина запускает операционную систему Windows.</span><span class="sxs-lookup"><span data-stu-id="c5212-112">This virtual machine runs the Windows operating system.</span></span>
<span data-ttu-id="c5212-113">Команда сохраняет данные в указанном локальном пути.</span><span class="sxs-lookup"><span data-stu-id="c5212-113">The command stores the data in specified local path.</span></span>

## <span data-ttu-id="c5212-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c5212-114">PARAMETERS</span></span>

### <span data-ttu-id="c5212-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5212-115">-DefaultProfile</span></span>
<span data-ttu-id="c5212-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c5212-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5212-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="c5212-117">-Linux</span></span>
<span data-ttu-id="c5212-118">Указывает на то, что виртуальная машина работает под управлением операционной системы Linux.</span><span class="sxs-lookup"><span data-stu-id="c5212-118">Indicates that the virtual machine runs the Linux operating system.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LinuxParamSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5212-119">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="c5212-119">-LocalPath</span></span>
<span data-ttu-id="c5212-120">Указывает локальный путь для данных диагностики загрузки.</span><span class="sxs-lookup"><span data-stu-id="c5212-120">Specifies the local path for the boot diagnostics data.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsParamSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: LinuxParamSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5212-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c5212-121">-Name</span></span>
<span data-ttu-id="c5212-122">Указывает имя виртуальной машины, для которой этот командлет получает данные диагностики.</span><span class="sxs-lookup"><span data-stu-id="c5212-122">Specifies the name of the virtual machine for which this cmdlet gets diagnostics data.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5212-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5212-123">-ResourceGroupName</span></span>
<span data-ttu-id="c5212-124">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c5212-124">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="c5212-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="c5212-125">-Windows</span></span>
<span data-ttu-id="c5212-126">Указывает на то, что виртуальная машина работает под управлением операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="c5212-126">Indicates that the virtual machine runs the Windows operating system.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsParamSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5212-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5212-127">CommonParameters</span></span>
<span data-ttu-id="c5212-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c5212-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5212-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c5212-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5212-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c5212-130">INPUTS</span></span>

### <span data-ttu-id="c5212-131">System. String</span><span class="sxs-lookup"><span data-stu-id="c5212-131">System.String</span></span>

## <span data-ttu-id="c5212-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c5212-132">OUTPUTS</span></span>

### <span data-ttu-id="c5212-133">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="c5212-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="c5212-134">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="c5212-134">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="c5212-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="c5212-135">NOTES</span></span>

## <span data-ttu-id="c5212-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c5212-136">RELATED LINKS</span></span>

[<span data-ttu-id="c5212-137">Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="c5212-137">Set-AzVMBootDiagnostics</span></span>](./Set-AzVMBootDiagnostics.md)


