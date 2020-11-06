---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D5BEA683-44AE-4D71-827D-02A03F0BEAE9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRMVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRMVMDiagnosticsExtension.md
ms.openlocfilehash: fbc357decbf4bdcd2e378294fed43125d38fd873
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561100"
---
# <span data-ttu-id="553a9-101">Get-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="553a9-101">Get-AzureRmVMDiagnosticsExtension</span></span>

## <span data-ttu-id="553a9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="553a9-102">SYNOPSIS</span></span>
<span data-ttu-id="553a9-103">Получает параметры расширения диагностики на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="553a9-103">Gets the settings of the Diagnostics extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="553a9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="553a9-104">SYNTAX</span></span>

```
Get-AzureRmVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="553a9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="553a9-105">DESCRIPTION</span></span>
<span data-ttu-id="553a9-106">Командлет **Get-AzureRmVMDiagnosticsExtension** получает параметры расширения диагностики Azure на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="553a9-106">The **Get-AzureRmVMDiagnosticsExtension** cmdlet gets the settings of the Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="553a9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="553a9-107">EXAMPLES</span></span>

### <span data-ttu-id="553a9-108">Пример 1: получение расширения диагностики, примененного к виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="553a9-108">Example 1: Get the diagnostics extension applied to a virtual machine</span></span>
```
PS C:\> Get-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22"
```

<span data-ttu-id="553a9-109">Эта команда получает расширение диагностики, примененное к виртуальной машине с именем ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="553a9-109">This command gets the diagnostics extension applied to the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="553a9-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="553a9-110">PARAMETERS</span></span>

### <span data-ttu-id="553a9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="553a9-111">-DefaultProfile</span></span>
<span data-ttu-id="553a9-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="553a9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="553a9-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="553a9-113">-Name</span></span>
<span data-ttu-id="553a9-114">Указывает имя расширения диагностики, для которого этот командлет получает параметры.</span><span class="sxs-lookup"><span data-stu-id="553a9-114">Specifies the name of the Diagnostics extension for which this cmdlet gets settings.</span></span>

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

### <span data-ttu-id="553a9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="553a9-115">-ResourceGroupName</span></span>
<span data-ttu-id="553a9-116">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="553a9-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="553a9-117">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="553a9-117">-Status</span></span>
<span data-ttu-id="553a9-118">Указывает на то, что этот командлет использует значение Status.</span><span class="sxs-lookup"><span data-stu-id="553a9-118">Indicates that this cmdlet uses the Status value.</span></span>

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

### <span data-ttu-id="553a9-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="553a9-119">-VMName</span></span>
<span data-ttu-id="553a9-120">Указывает имя виртуальной машины, с помощью которой этот командлет получает расширение диагностики.</span><span class="sxs-lookup"><span data-stu-id="553a9-120">Specifies the name of the virtual machine from which this cmdlet gets the Diagnostics extension.</span></span>

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

### <span data-ttu-id="553a9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="553a9-121">CommonParameters</span></span>
<span data-ttu-id="553a9-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="553a9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="553a9-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="553a9-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="553a9-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="553a9-124">INPUTS</span></span>

### <span data-ttu-id="553a9-125">System. String</span><span class="sxs-lookup"><span data-stu-id="553a9-125">System.String</span></span>

### <span data-ttu-id="553a9-126">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="553a9-126">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="553a9-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="553a9-127">OUTPUTS</span></span>

### <span data-ttu-id="553a9-128">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="553a9-128">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="553a9-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="553a9-129">NOTES</span></span>

## <span data-ttu-id="553a9-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="553a9-130">RELATED LINKS</span></span>

[<span data-ttu-id="553a9-131">Remove-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="553a9-131">Remove-AzureRmVMDiagnosticsExtension</span></span>](./Remove-AzureRmVMDiagnosticsExtension.md)

[<span data-ttu-id="553a9-132">Set-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="553a9-132">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)


