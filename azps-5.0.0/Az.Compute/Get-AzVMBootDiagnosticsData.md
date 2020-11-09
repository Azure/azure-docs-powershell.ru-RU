---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 15CAC050-F2E9-4872-88E7-516A6D194FAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmbootdiagnosticsdata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMBootDiagnosticsData.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMBootDiagnosticsData.md
ms.openlocfilehash: 96248492feac9997d1afdba83fdda943c75fa363
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249407"
---
# <span data-ttu-id="99d0e-101">Get-AzVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="99d0e-101">Get-AzVMBootDiagnosticsData</span></span>

## <span data-ttu-id="99d0e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="99d0e-102">SYNOPSIS</span></span>
<span data-ttu-id="99d0e-103">Получение данных диагностики загрузки для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="99d0e-103">Gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="99d0e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="99d0e-104">SYNTAX</span></span>

### <span data-ttu-id="99d0e-105">WindowsParamSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="99d0e-105">WindowsParamSet (Default)</span></span>
```
Get-AzVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Windows] [-LocalPath] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99d0e-106">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="99d0e-106">LinuxParamSet</span></span>
```
Get-AzVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Linux] [[-LocalPath] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99d0e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="99d0e-107">DESCRIPTION</span></span>
<span data-ttu-id="99d0e-108">Командлет **Get-AzVMBootDiagnosticsData** получает данные диагностики загрузки для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="99d0e-108">The **Get-AzVMBootDiagnosticsData** cmdlet gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="99d0e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="99d0e-109">EXAMPLES</span></span>

### <span data-ttu-id="99d0e-110">Пример 1: получение данных диагностики загрузки</span><span class="sxs-lookup"><span data-stu-id="99d0e-110">Example 1: Get boot diagnostics data</span></span>
```
PS C:\> Get-AzVMBootDiagnosticsData -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07" -Windows -LocalPath "C:\Contoso\BootDiagnostics"
```

<span data-ttu-id="99d0e-111">Эта команда возвращает данные диагностики загрузки для виртуальной машины с именем ContosoVM07.</span><span class="sxs-lookup"><span data-stu-id="99d0e-111">This command gets boot diagnostics data for the virtual machine named ContosoVM07.</span></span>
<span data-ttu-id="99d0e-112">Эта виртуальная машина запускает операционную систему Windows.</span><span class="sxs-lookup"><span data-stu-id="99d0e-112">This virtual machine runs the Windows operating system.</span></span>
<span data-ttu-id="99d0e-113">Команда сохраняет данные в указанном локальном пути.</span><span class="sxs-lookup"><span data-stu-id="99d0e-113">The command stores the data in specified local path.</span></span>

## <span data-ttu-id="99d0e-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="99d0e-114">PARAMETERS</span></span>

### <span data-ttu-id="99d0e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99d0e-115">-DefaultProfile</span></span>
<span data-ttu-id="99d0e-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="99d0e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99d0e-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="99d0e-117">-Linux</span></span>
<span data-ttu-id="99d0e-118">Указывает на то, что виртуальная машина работает под управлением операционной системы Linux.</span><span class="sxs-lookup"><span data-stu-id="99d0e-118">Indicates that the virtual machine runs the Linux operating system.</span></span>

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

### <span data-ttu-id="99d0e-119">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="99d0e-119">-LocalPath</span></span>
<span data-ttu-id="99d0e-120">Указывает локальный путь для данных диагностики загрузки.</span><span class="sxs-lookup"><span data-stu-id="99d0e-120">Specifies the local path for the boot diagnostics data.</span></span>

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

### <span data-ttu-id="99d0e-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="99d0e-121">-Name</span></span>
<span data-ttu-id="99d0e-122">Указывает имя виртуальной машины, для которой этот командлет получает данные диагностики.</span><span class="sxs-lookup"><span data-stu-id="99d0e-122">Specifies the name of the virtual machine for which this cmdlet gets diagnostics data.</span></span>

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

### <span data-ttu-id="99d0e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99d0e-123">-ResourceGroupName</span></span>
<span data-ttu-id="99d0e-124">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="99d0e-124">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="99d0e-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="99d0e-125">-Windows</span></span>
<span data-ttu-id="99d0e-126">Указывает на то, что виртуальная машина работает под управлением операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="99d0e-126">Indicates that the virtual machine runs the Windows operating system.</span></span>

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

### <span data-ttu-id="99d0e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99d0e-127">CommonParameters</span></span>
<span data-ttu-id="99d0e-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="99d0e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99d0e-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="99d0e-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99d0e-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="99d0e-130">INPUTS</span></span>

### <span data-ttu-id="99d0e-131">System. String</span><span class="sxs-lookup"><span data-stu-id="99d0e-131">System.String</span></span>

## <span data-ttu-id="99d0e-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="99d0e-132">OUTPUTS</span></span>

### <span data-ttu-id="99d0e-133">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="99d0e-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="99d0e-134">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="99d0e-134">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="99d0e-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="99d0e-135">NOTES</span></span>

## <span data-ttu-id="99d0e-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="99d0e-136">RELATED LINKS</span></span>

[<span data-ttu-id="99d0e-137">Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="99d0e-137">Set-AzVMBootDiagnostic</span></span>](./Set-AzVMBootDiagnostic.md)

