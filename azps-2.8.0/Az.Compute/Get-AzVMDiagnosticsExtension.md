---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D5BEA683-44AE-4D71-827D-02A03F0BEAE9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiagnosticsExtension.md
ms.openlocfilehash: 6b857356ea35476117a58f8f31f7174a7a91767a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721919"
---
# <span data-ttu-id="a741b-101">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="a741b-101">Get-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="a741b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a741b-102">SYNOPSIS</span></span>
<span data-ttu-id="a741b-103">Получает параметры расширения диагностики на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="a741b-103">Gets the settings of the Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="a741b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a741b-104">SYNTAX</span></span>

```
Get-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a741b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a741b-105">DESCRIPTION</span></span>
<span data-ttu-id="a741b-106">Командлет **Get-AzVMDiagnosticsExtension** получает параметры расширения диагностики Azure на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="a741b-106">The **Get-AzVMDiagnosticsExtension** cmdlet gets the settings of the Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="a741b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a741b-107">EXAMPLES</span></span>

### <span data-ttu-id="a741b-108">Пример 1: получение расширения диагностики, примененного к виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="a741b-108">Example 1: Get the diagnostics extension applied to a virtual machine</span></span>
```
PS C:\> Get-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22"
```

<span data-ttu-id="a741b-109">Эта команда получает расширение диагностики, примененное к виртуальной машине с именем ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="a741b-109">This command gets the diagnostics extension applied to the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="a741b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a741b-110">PARAMETERS</span></span>

### <span data-ttu-id="a741b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a741b-111">-DefaultProfile</span></span>
<span data-ttu-id="a741b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a741b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a741b-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a741b-113">-Name</span></span>
<span data-ttu-id="a741b-114">Указывает имя расширения диагностики, для которого этот командлет получает параметры.</span><span class="sxs-lookup"><span data-stu-id="a741b-114">Specifies the name of the Diagnostics extension for which this cmdlet gets settings.</span></span>

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

### <span data-ttu-id="a741b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a741b-115">-ResourceGroupName</span></span>
<span data-ttu-id="a741b-116">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a741b-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="a741b-117">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="a741b-117">-Status</span></span>
<span data-ttu-id="a741b-118">Указывает на то, что этот командлет использует значение Status.</span><span class="sxs-lookup"><span data-stu-id="a741b-118">Indicates that this cmdlet uses the Status value.</span></span>

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

### <span data-ttu-id="a741b-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="a741b-119">-VMName</span></span>
<span data-ttu-id="a741b-120">Указывает имя виртуальной машины, с помощью которой этот командлет получает расширение диагностики.</span><span class="sxs-lookup"><span data-stu-id="a741b-120">Specifies the name of the virtual machine from which this cmdlet gets the Diagnostics extension.</span></span>

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

### <span data-ttu-id="a741b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a741b-121">CommonParameters</span></span>
<span data-ttu-id="a741b-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a741b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a741b-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a741b-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a741b-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a741b-124">INPUTS</span></span>

### <span data-ttu-id="a741b-125">System. String</span><span class="sxs-lookup"><span data-stu-id="a741b-125">System.String</span></span>

### <span data-ttu-id="a741b-126">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a741b-126">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a741b-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a741b-127">OUTPUTS</span></span>

### <span data-ttu-id="a741b-128">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="a741b-128">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="a741b-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="a741b-129">NOTES</span></span>

## <span data-ttu-id="a741b-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a741b-130">RELATED LINKS</span></span>

[<span data-ttu-id="a741b-131">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="a741b-131">Remove-AzVMDiagnosticsExtension</span></span>](./Remove-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="a741b-132">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="a741b-132">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)


