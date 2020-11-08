---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D5BEA683-44AE-4D71-827D-02A03F0BEAE9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiagnosticsExtension.md
ms.openlocfilehash: bd56d9e76ffc71d75de0a29fa40291cb405e57fe
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94075052"
---
# <span data-ttu-id="88303-101">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="88303-101">Get-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="88303-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="88303-102">SYNOPSIS</span></span>
<span data-ttu-id="88303-103">Получает параметры расширения диагностики на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="88303-103">Gets the settings of the Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="88303-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="88303-104">SYNTAX</span></span>

```
Get-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88303-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="88303-105">DESCRIPTION</span></span>
<span data-ttu-id="88303-106">Командлет **Get-AzVMDiagnosticsExtension** получает параметры расширения диагностики Azure на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="88303-106">The **Get-AzVMDiagnosticsExtension** cmdlet gets the settings of the Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="88303-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="88303-107">EXAMPLES</span></span>

### <span data-ttu-id="88303-108">Пример 1: получение расширения диагностики, примененного к виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="88303-108">Example 1: Get the diagnostics extension applied to a virtual machine</span></span>
```
PS C:\> Get-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22"
```

<span data-ttu-id="88303-109">Эта команда получает расширение диагностики, примененное к виртуальной машине с именем ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="88303-109">This command gets the diagnostics extension applied to the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="88303-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="88303-110">PARAMETERS</span></span>

### <span data-ttu-id="88303-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88303-111">-DefaultProfile</span></span>
<span data-ttu-id="88303-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="88303-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88303-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="88303-113">-Name</span></span>
<span data-ttu-id="88303-114">Указывает имя расширения диагностики, для которого этот командлет получает параметры.</span><span class="sxs-lookup"><span data-stu-id="88303-114">Specifies the name of the Diagnostics extension for which this cmdlet gets settings.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88303-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88303-115">-ResourceGroupName</span></span>
<span data-ttu-id="88303-116">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="88303-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="88303-117">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="88303-117">-Status</span></span>
<span data-ttu-id="88303-118">Указывает на то, что этот командлет использует значение Status.</span><span class="sxs-lookup"><span data-stu-id="88303-118">Indicates that this cmdlet uses the Status value.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88303-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="88303-119">-VMName</span></span>
<span data-ttu-id="88303-120">Указывает имя виртуальной машины, с помощью которой этот командлет получает расширение диагностики.</span><span class="sxs-lookup"><span data-stu-id="88303-120">Specifies the name of the virtual machine from which this cmdlet gets the Diagnostics extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88303-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88303-121">CommonParameters</span></span>
<span data-ttu-id="88303-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="88303-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88303-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="88303-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88303-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="88303-124">INPUTS</span></span>

### <span data-ttu-id="88303-125">System. String</span><span class="sxs-lookup"><span data-stu-id="88303-125">System.String</span></span>

### <span data-ttu-id="88303-126">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="88303-126">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="88303-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="88303-127">OUTPUTS</span></span>

### <span data-ttu-id="88303-128">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="88303-128">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="88303-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="88303-129">NOTES</span></span>

## <span data-ttu-id="88303-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="88303-130">RELATED LINKS</span></span>

[<span data-ttu-id="88303-131">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="88303-131">Remove-AzVMDiagnosticsExtension</span></span>](./Remove-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="88303-132">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="88303-132">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)


