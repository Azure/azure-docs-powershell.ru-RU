---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 15CAC050-F2E9-4872-88E7-516A6D194FAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmbootdiagnosticsdata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMBootDiagnosticsData.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMBootDiagnosticsData.md
ms.openlocfilehash: ab7bae5430bf2b588997d57e92a18a4408ca4334
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911540"
---
# <span data-ttu-id="3109e-101">Get-AzVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="3109e-101">Get-AzVMBootDiagnosticsData</span></span>

## <span data-ttu-id="3109e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3109e-102">SYNOPSIS</span></span>
<span data-ttu-id="3109e-103">Получение данных диагностики загрузки для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="3109e-103">Gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="3109e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3109e-104">SYNTAX</span></span>

### <span data-ttu-id="3109e-105">WindowsParamSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3109e-105">WindowsParamSet (Default)</span></span>
```
Get-AzVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Windows]
 [-LocalPath] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3109e-106">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="3109e-106">LinuxParamSet</span></span>
```
Get-AzVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Linux]
 [[-LocalPath] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3109e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3109e-107">DESCRIPTION</span></span>
<span data-ttu-id="3109e-108">Командлет **Get-AzVMBootDiagnosticsData** получает данные диагностики загрузки для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="3109e-108">The **Get-AzVMBootDiagnosticsData** cmdlet gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="3109e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3109e-109">EXAMPLES</span></span>

### <span data-ttu-id="3109e-110">Пример 1: получение данных диагностики загрузки</span><span class="sxs-lookup"><span data-stu-id="3109e-110">Example 1: Get boot diagnostics data</span></span>
```
PS C:\> Get-AzVMBootDiagnosticsData -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07" -Windows -LocalPath "C:\Contoso\BootDiagnostics"
```

<span data-ttu-id="3109e-111">Эта команда возвращает данные диагностики загрузки для виртуальной машины с именем ContosoVM07.</span><span class="sxs-lookup"><span data-stu-id="3109e-111">This command gets boot diagnostics data for the virtual machine named ContosoVM07.</span></span>
<span data-ttu-id="3109e-112">Эта виртуальная машина запускает операционную систему Windows.</span><span class="sxs-lookup"><span data-stu-id="3109e-112">This virtual machine runs the Windows operating system.</span></span>
<span data-ttu-id="3109e-113">Команда сохраняет данные в указанном локальном пути.</span><span class="sxs-lookup"><span data-stu-id="3109e-113">The command stores the data in specified local path.</span></span>

## <span data-ttu-id="3109e-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3109e-114">PARAMETERS</span></span>

### <span data-ttu-id="3109e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3109e-115">-DefaultProfile</span></span>
<span data-ttu-id="3109e-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3109e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3109e-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="3109e-117">-Linux</span></span>
<span data-ttu-id="3109e-118">Указывает на то, что виртуальная машина работает под управлением операционной системы Linux.</span><span class="sxs-lookup"><span data-stu-id="3109e-118">Indicates that the virtual machine runs the Linux operating system.</span></span>

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

### <span data-ttu-id="3109e-119">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="3109e-119">-LocalPath</span></span>
<span data-ttu-id="3109e-120">Указывает локальный путь для данных диагностики загрузки.</span><span class="sxs-lookup"><span data-stu-id="3109e-120">Specifies the local path for the boot diagnostics data.</span></span>

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

### <span data-ttu-id="3109e-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3109e-121">-Name</span></span>
<span data-ttu-id="3109e-122">Указывает имя виртуальной машины, для которой этот командлет получает данные диагностики.</span><span class="sxs-lookup"><span data-stu-id="3109e-122">Specifies the name of the virtual machine for which this cmdlet gets diagnostics data.</span></span>

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

### <span data-ttu-id="3109e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3109e-123">-ResourceGroupName</span></span>
<span data-ttu-id="3109e-124">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="3109e-124">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="3109e-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="3109e-125">-Windows</span></span>
<span data-ttu-id="3109e-126">Указывает на то, что виртуальная машина работает под управлением операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="3109e-126">Indicates that the virtual machine runs the Windows operating system.</span></span>

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

### <span data-ttu-id="3109e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3109e-127">CommonParameters</span></span>
<span data-ttu-id="3109e-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3109e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3109e-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3109e-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3109e-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3109e-130">INPUTS</span></span>

### <span data-ttu-id="3109e-131">Ничего</span><span class="sxs-lookup"><span data-stu-id="3109e-131">None</span></span>
<span data-ttu-id="3109e-132">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="3109e-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3109e-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3109e-133">OUTPUTS</span></span>

### <span data-ttu-id="3109e-134">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="3109e-134">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="3109e-135">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="3109e-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="3109e-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="3109e-136">NOTES</span></span>

## <span data-ttu-id="3109e-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3109e-137">RELATED LINKS</span></span>

[<span data-ttu-id="3109e-138">Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="3109e-138">Set-AzVMBootDiagnostic</span></span>](./Set-AzVMBootDiagnostic.md)


