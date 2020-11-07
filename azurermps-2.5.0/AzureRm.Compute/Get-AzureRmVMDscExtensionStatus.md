---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 695F224D-DA25-49F2-916E-25DA2A48A4A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmdscextensionstatus
schema: 2.0.0
ms.openlocfilehash: b6ec9918657c191e31e10c04b799603654d39d56
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913394"
---
# <span data-ttu-id="25b56-101">Get-AzureRmVMDscExtensionStatus</span><span class="sxs-lookup"><span data-stu-id="25b56-101">Get-AzureRmVMDscExtensionStatus</span></span>

## <span data-ttu-id="25b56-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="25b56-102">SYNOPSIS</span></span>
<span data-ttu-id="25b56-103">Возвращает состояние обработчика расширений DSC для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="25b56-103">Gets the status of the DSC extension handler for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25b56-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="25b56-104">SYNTAX</span></span>

```
Get-AzureRmVMDscExtensionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25b56-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="25b56-105">DESCRIPTION</span></span>
<span data-ttu-id="25b56-106">Командлет **Get-AzureRmVMDscExtensionStatus** получает состояние обработчика расширения необходимой конфигурации состояния (DSC) для виртуальной машины в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="25b56-106">The **Get-AzureRmVMDscExtensionStatus** cmdlet gets the status of the Desired State Configuration (DSC) extension handler for a virtual machine in a resource group.</span></span>
<span data-ttu-id="25b56-107">При применении конфигурации этот командлет создает данные, которые будут выводиться в соответствии с командлетом Start-DscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="25b56-107">When a configuration is applied this cmdlet produces output consistent with the Start-DscConfiguration cmdlet.</span></span>

## <span data-ttu-id="25b56-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="25b56-108">EXAMPLES</span></span>

### <span data-ttu-id="25b56-109">1:</span><span class="sxs-lookup"><span data-stu-id="25b56-109">1:</span></span>
```

```

## <span data-ttu-id="25b56-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="25b56-110">PARAMETERS</span></span>

### <span data-ttu-id="25b56-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25b56-111">-DefaultProfile</span></span>
<span data-ttu-id="25b56-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="25b56-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25b56-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="25b56-113">-Name</span></span>
<span data-ttu-id="25b56-114">Указывает имя ресурса диспетчера ресурсов Azure, представляющего расширение.</span><span class="sxs-lookup"><span data-stu-id="25b56-114">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="25b56-115">Командлет Set-AzureRmVMDscExtension задает для этого имени имя Microsoft. PowerShell. DSC, которое совпадает со значением, которое используется для **Get-AzureRmVMDscExtensionStatus**.</span><span class="sxs-lookup"><span data-stu-id="25b56-115">The Set-AzureRmVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzureRmVMDscExtensionStatus**.</span></span>
<span data-ttu-id="25b56-116">Указывайте этот параметр только в том случае, если вы изменили имя по умолчанию в командлете Set или использовали другое имя ресурса в шаблоне диспетчера ресурсов.</span><span class="sxs-lookup"><span data-stu-id="25b56-116">Specify this parameter only if you changed the default name in the Set cmdlet or used a different resource name in a Resource Manager template.</span></span>

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

### <span data-ttu-id="25b56-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25b56-117">-ResourceGroupName</span></span>
<span data-ttu-id="25b56-118">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="25b56-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="25b56-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="25b56-119">-VMName</span></span>
<span data-ttu-id="25b56-120">Указывает имя виртуальной машины, для которой этот командлет получает состояние расширения DSC.</span><span class="sxs-lookup"><span data-stu-id="25b56-120">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension status.</span></span>

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

### <span data-ttu-id="25b56-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25b56-121">CommonParameters</span></span>
<span data-ttu-id="25b56-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="25b56-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25b56-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25b56-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25b56-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="25b56-124">INPUTS</span></span>

### <span data-ttu-id="25b56-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="25b56-125">None</span></span>
<span data-ttu-id="25b56-126">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="25b56-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="25b56-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="25b56-127">OUTPUTS</span></span>

### <span data-ttu-id="25b56-128">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="25b56-128">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="25b56-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="25b56-129">NOTES</span></span>

## <span data-ttu-id="25b56-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="25b56-130">RELATED LINKS</span></span>

[<span data-ttu-id="25b56-131">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="25b56-131">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)


