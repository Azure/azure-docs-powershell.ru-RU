---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 32CF9DA7-5607-4CF9-A2D0-D76A0C005FDA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMAccessExtension.md
ms.openlocfilehash: 9e7cb85bf29d6982271768af6948db1d3c5b8605
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561912"
---
# <span data-ttu-id="5108e-101">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="5108e-101">Get-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="5108e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5108e-102">SYNOPSIS</span></span>
<span data-ttu-id="5108e-103">Получает сведения о расширении VMAccess.</span><span class="sxs-lookup"><span data-stu-id="5108e-103">Gets information about the VMAccess extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5108e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5108e-104">SYNTAX</span></span>

```
Get-AzureRmVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [<CommonParameters>]
```

## <span data-ttu-id="5108e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5108e-105">DESCRIPTION</span></span>
<span data-ttu-id="5108e-106">Командлет **Get-AzureRmVMAccessExtension** получает сведения о расширении виртуальной машины доступа к виртуальной машине (VMAccess).</span><span class="sxs-lookup"><span data-stu-id="5108e-106">The **Get-AzureRmVMAccessExtension** cmdlet gets information about the Virtual Machine Access (VMAccess) Virtual Machine Extension.</span></span>

## <span data-ttu-id="5108e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5108e-107">EXAMPLES</span></span>

### <span data-ttu-id="5108e-108">Пример 1: получение расширения VMAccess</span><span class="sxs-lookup"><span data-stu-id="5108e-108">Example 1: Get the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzureRmVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest"
```

<span data-ttu-id="5108e-109">Эта команда получает расширение VMAccess с именем ContosoTest для виртуальной машины с именем VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="5108e-109">This command gets the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="5108e-110">Пример 2: получение представления экземпляра расширения VMAccess</span><span class="sxs-lookup"><span data-stu-id="5108e-110">Example 2: Get the instance view of the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzureRmVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest" -Status
```

<span data-ttu-id="5108e-111">Эта команда получает представление экземпляра расширения VMAccess с именем ContosoTest для виртуальной машины с именем VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="5108e-111">This command gets the instance view of the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="5108e-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5108e-112">PARAMETERS</span></span>

### <span data-ttu-id="5108e-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5108e-113">-Name</span></span>
<span data-ttu-id="5108e-114">Указывает имя расширения, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="5108e-114">Specifies the name of the extension that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5108e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5108e-115">-ResourceGroupName</span></span>
<span data-ttu-id="5108e-116">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5108e-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="5108e-117">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="5108e-117">-Status</span></span>
<span data-ttu-id="5108e-118">Указывает на то, что этот командлет получает только представление экземпляра расширения.</span><span class="sxs-lookup"><span data-stu-id="5108e-118">Indicates that this cmdlet gets only the instance view of the extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5108e-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="5108e-119">-VMName</span></span>
<span data-ttu-id="5108e-120">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5108e-120">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="5108e-121">Этот командлет получает сведения о VMAccess для виртуальной машины, указывающей этот параметр.</span><span class="sxs-lookup"><span data-stu-id="5108e-121">This cmdlet gets information about VMAccess for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5108e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5108e-122">CommonParameters</span></span>
<span data-ttu-id="5108e-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5108e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5108e-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5108e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5108e-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5108e-125">INPUTS</span></span>

### <span data-ttu-id="5108e-126">Ничего</span><span class="sxs-lookup"><span data-stu-id="5108e-126">None</span></span>
<span data-ttu-id="5108e-127">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="5108e-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5108e-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5108e-128">OUTPUTS</span></span>

## <span data-ttu-id="5108e-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="5108e-129">NOTES</span></span>

## <span data-ttu-id="5108e-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5108e-130">RELATED LINKS</span></span>

[<span data-ttu-id="5108e-131">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="5108e-131">Remove-AzureRmVMAccessExtension</span></span>](./Remove-AzureRmVMAccessExtension.md)

[<span data-ttu-id="5108e-132">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="5108e-132">Set-AzureRmVMAccessExtension</span></span>](./Set-AzureRmVMAccessExtension.md)

[<span data-ttu-id="5108e-133">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="5108e-133">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)


