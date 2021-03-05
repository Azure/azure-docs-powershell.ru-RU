---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 15CAC050-F2E9-4872-88E7-516A6D194FAB
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmbootdiagnosticsdata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMBootDiagnosticsData.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMBootDiagnosticsData.md
ms.openlocfilehash: 539e8b0a91c72d275f0997f2ebc69e86f4a9c901
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013864"
---
# <span data-ttu-id="cb42a-101">Get-AzVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="cb42a-101">Get-AzVMBootDiagnosticsData</span></span>

## <span data-ttu-id="cb42a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb42a-102">SYNOPSIS</span></span>
<span data-ttu-id="cb42a-103">Загружает диагностические данные для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="cb42a-103">Gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="cb42a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cb42a-104">SYNTAX</span></span>

### <span data-ttu-id="cb42a-105">WindowsParamSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cb42a-105">WindowsParamSet (Default)</span></span>
```
Get-AzVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Windows] [-LocalPath] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb42a-106">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="cb42a-106">LinuxParamSet</span></span>
```
Get-AzVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Linux] [[-LocalPath] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb42a-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cb42a-107">DESCRIPTION</span></span>
<span data-ttu-id="cb42a-108">Cmdlet **Get-AzVMBootDiagnosticsData** получает диагностические данные для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="cb42a-108">The **Get-AzVMBootDiagnosticsData** cmdlet gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="cb42a-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cb42a-109">EXAMPLES</span></span>

### <span data-ttu-id="cb42a-110">Пример 1. Загрузка диагностических данных</span><span class="sxs-lookup"><span data-stu-id="cb42a-110">Example 1: Get boot diagnostics data</span></span>
```
PS C:\> Get-AzVMBootDiagnosticsData -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07" -Windows -LocalPath "C:\Contoso\BootDiagnostics"
```

<span data-ttu-id="cb42a-111">Эта команда загружает диагностические данные для виртуальной машины с именем ContosoVM07.</span><span class="sxs-lookup"><span data-stu-id="cb42a-111">This command gets boot diagnostics data for the virtual machine named ContosoVM07.</span></span>
<span data-ttu-id="cb42a-112">На этой виртуальной машине работает операционная система Windows.</span><span class="sxs-lookup"><span data-stu-id="cb42a-112">This virtual machine runs the Windows operating system.</span></span>
<span data-ttu-id="cb42a-113">Команда хранит данные в указанном локальном пути.</span><span class="sxs-lookup"><span data-stu-id="cb42a-113">The command stores the data in specified local path.</span></span>

## <span data-ttu-id="cb42a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb42a-114">PARAMETERS</span></span>

### <span data-ttu-id="cb42a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb42a-115">-DefaultProfile</span></span>
<span data-ttu-id="cb42a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cb42a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb42a-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="cb42a-117">-Linux</span></span>
<span data-ttu-id="cb42a-118">Указывает на то, что на виртуальной машине работает операционная система Linux.</span><span class="sxs-lookup"><span data-stu-id="cb42a-118">Indicates that the virtual machine runs the Linux operating system.</span></span>

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

### <span data-ttu-id="cb42a-119">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="cb42a-119">-LocalPath</span></span>
<span data-ttu-id="cb42a-120">Указывает локальный путь для диагностических данных загрузки.</span><span class="sxs-lookup"><span data-stu-id="cb42a-120">Specifies the local path for the boot diagnostics data.</span></span>

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

### <span data-ttu-id="cb42a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="cb42a-121">-Name</span></span>
<span data-ttu-id="cb42a-122">Указывает имя виртуальной машины, для которой этот cmdlet получает диагностические данные.</span><span class="sxs-lookup"><span data-stu-id="cb42a-122">Specifies the name of the virtual machine for which this cmdlet gets diagnostics data.</span></span>

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

### <span data-ttu-id="cb42a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb42a-123">-ResourceGroupName</span></span>
<span data-ttu-id="cb42a-124">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="cb42a-124">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="cb42a-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="cb42a-125">-Windows</span></span>
<span data-ttu-id="cb42a-126">Указывает на то, что на виртуальной машине работает операционная система Windows.</span><span class="sxs-lookup"><span data-stu-id="cb42a-126">Indicates that the virtual machine runs the Windows operating system.</span></span>

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

### <span data-ttu-id="cb42a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb42a-127">CommonParameters</span></span>
<span data-ttu-id="cb42a-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb42a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb42a-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cb42a-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb42a-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cb42a-130">INPUTS</span></span>

### <span data-ttu-id="cb42a-131">System.String</span><span class="sxs-lookup"><span data-stu-id="cb42a-131">System.String</span></span>

## <span data-ttu-id="cb42a-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cb42a-132">OUTPUTS</span></span>

### <span data-ttu-id="cb42a-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelse</span><span class="sxs-lookup"><span data-stu-id="cb42a-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="cb42a-134">Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelseInstanceView</span><span class="sxs-lookup"><span data-stu-id="cb42a-134">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="cb42a-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cb42a-135">NOTES</span></span>

## <span data-ttu-id="cb42a-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cb42a-136">RELATED LINKS</span></span>

[<span data-ttu-id="cb42a-137">Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="cb42a-137">Set-AzVMBootDiagnostic</span></span>](./Set-AzVMBootDiagnostic.md)


