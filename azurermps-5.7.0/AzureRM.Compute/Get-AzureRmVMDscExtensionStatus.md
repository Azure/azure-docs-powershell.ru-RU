---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 695F224D-DA25-49F2-916E-25DA2A48A4A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDscExtensionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDscExtensionStatus.md
ms.openlocfilehash: 7cb7f175cc15e7d4e0915b6af9ef6fe6bdfc74d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559211"
---
# <span data-ttu-id="9e510-101">Get-AzureRmVMDscExtensionStatus</span><span class="sxs-lookup"><span data-stu-id="9e510-101">Get-AzureRmVMDscExtensionStatus</span></span>

## <span data-ttu-id="9e510-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9e510-102">SYNOPSIS</span></span>
<span data-ttu-id="9e510-103">Возвращает состояние обработчика расширений DSC для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9e510-103">Gets the status of the DSC extension handler for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e510-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9e510-104">SYNTAX</span></span>

```
Get-AzureRmVMDscExtensionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="9e510-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e510-105">DESCRIPTION</span></span>
<span data-ttu-id="9e510-106">Командлет **Get-AzureRmVMDscExtensionStatus** получает состояние обработчика расширения необходимой конфигурации состояния (DSC) для виртуальной машины в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9e510-106">The **Get-AzureRmVMDscExtensionStatus** cmdlet gets the status of the Desired State Configuration (DSC) extension handler for a virtual machine in a resource group.</span></span>
<span data-ttu-id="9e510-107">При применении конфигурации этот командлет создает данные, которые будут выводиться в соответствии с командлетом Start-DscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="9e510-107">When a configuration is applied this cmdlet produces output consistent with the Start-DscConfiguration cmdlet.</span></span>

## <span data-ttu-id="9e510-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9e510-108">EXAMPLES</span></span>

## <span data-ttu-id="9e510-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9e510-109">PARAMETERS</span></span>

### <span data-ttu-id="9e510-110">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9e510-110">-Name</span></span>
<span data-ttu-id="9e510-111">Указывает имя ресурса диспетчера ресурсов Azure, представляющего расширение.</span><span class="sxs-lookup"><span data-stu-id="9e510-111">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="9e510-112">Командлет Set-AzureRmVMDscExtension задает для этого имени имя Microsoft. PowerShell. DSC, которое совпадает со значением, которое используется для **Get-AzureRmVMDscExtensionStatus**.</span><span class="sxs-lookup"><span data-stu-id="9e510-112">The Set-AzureRmVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzureRmVMDscExtensionStatus**.</span></span>
<span data-ttu-id="9e510-113">Указывайте этот параметр только в том случае, если вы изменили имя по умолчанию в командлете Set или использовали другое имя ресурса в шаблоне диспетчера ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9e510-113">Specify this parameter only if you changed the default name in the Set cmdlet or used a different resource name in a Resource Manager template.</span></span>

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

### <span data-ttu-id="9e510-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e510-114">-ResourceGroupName</span></span>
<span data-ttu-id="9e510-115">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9e510-115">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="9e510-116">-VMName</span><span class="sxs-lookup"><span data-stu-id="9e510-116">-VMName</span></span>
<span data-ttu-id="9e510-117">Указывает имя виртуальной машины, для которой этот командлет получает состояние расширения DSC.</span><span class="sxs-lookup"><span data-stu-id="9e510-117">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension status.</span></span>

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

### <span data-ttu-id="9e510-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e510-118">CommonParameters</span></span>
<span data-ttu-id="9e510-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9e510-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e510-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e510-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e510-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9e510-121">INPUTS</span></span>

### <span data-ttu-id="9e510-122">Ничего</span><span class="sxs-lookup"><span data-stu-id="9e510-122">None</span></span>
<span data-ttu-id="9e510-123">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="9e510-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9e510-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e510-124">OUTPUTS</span></span>

## <span data-ttu-id="9e510-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="9e510-125">NOTES</span></span>

## <span data-ttu-id="9e510-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9e510-126">RELATED LINKS</span></span>

[<span data-ttu-id="9e510-127">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="9e510-127">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)


