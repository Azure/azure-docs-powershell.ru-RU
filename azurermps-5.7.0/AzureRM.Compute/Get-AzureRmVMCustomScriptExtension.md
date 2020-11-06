---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 1017A74D-6420-4E51-A4A4-1AD3AD6D8122
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMCustomScriptExtension.md
ms.openlocfilehash: 1f348a7cddc31a2a3d3d255aa6b4fe80d1808f36
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563703"
---
# <span data-ttu-id="59362-101">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="59362-101">Get-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="59362-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="59362-102">SYNOPSIS</span></span>
<span data-ttu-id="59362-103">Получает сведения о настраиваемом расширении сценария.</span><span class="sxs-lookup"><span data-stu-id="59362-103">Gets information about a custom script extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59362-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="59362-104">SYNTAX</span></span>

```
Get-AzureRmVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [<CommonParameters>]
```

## <span data-ttu-id="59362-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="59362-105">DESCRIPTION</span></span>
<span data-ttu-id="59362-106">Командлет **Get-AzureRmVMCustomScriptExtension** получает сведения о расширении виртуальной машины настраиваемого сценария на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="59362-106">The **Get-AzureRmVMCustomScriptExtension** cmdlet gets information about a custom script Virtual Machine Extension on a virtual machine.</span></span>

## <span data-ttu-id="59362-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="59362-107">EXAMPLES</span></span>

### <span data-ttu-id="59362-108">Пример 1: получение расширения настраиваемого сценария</span><span class="sxs-lookup"><span data-stu-id="59362-108">Example 1: Get a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzureRmVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript"
```

<span data-ttu-id="59362-109">Эта команда получает настраиваемое расширение сценария с именем ContosoCustomScript для виртуальной машины с именем VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="59362-109">This command gets the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="59362-110">Пример 2: получение представления экземпляра настраиваемого расширения сценария</span><span class="sxs-lookup"><span data-stu-id="59362-110">Example 2: Get the instance view of a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzureRmVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript" -Status
```

<span data-ttu-id="59362-111">Эта команда получает представление экземпляра настраиваемого расширения сценария с именем ContosoCustomScript для виртуальной машины с именем VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="59362-111">This command gets the instance view of the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="59362-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="59362-112">PARAMETERS</span></span>

### <span data-ttu-id="59362-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="59362-113">-Name</span></span>
<span data-ttu-id="59362-114">Указывает имя настраиваемого расширения сценария, для которого этот командлет получает сведения.</span><span class="sxs-lookup"><span data-stu-id="59362-114">Specifies the name of the custom script extension about which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="59362-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59362-115">-ResourceGroupName</span></span>
<span data-ttu-id="59362-116">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="59362-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="59362-117">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="59362-117">-Status</span></span>
<span data-ttu-id="59362-118">Указывает на то, что этот командлет получает представление экземпляра для расширения настраиваемого сценария.</span><span class="sxs-lookup"><span data-stu-id="59362-118">Indicates that this cmdlet gets the instance view of the custom script extension.</span></span>

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

### <span data-ttu-id="59362-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="59362-119">-VMName</span></span>
<span data-ttu-id="59362-120">Указывает имя виртуальной машины, для которой этот командлет получает настраиваемое расширение сценария.</span><span class="sxs-lookup"><span data-stu-id="59362-120">Specifies the name of a virtual machine for which this cmdlet gets the custom script extension.</span></span>

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

### <span data-ttu-id="59362-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59362-121">CommonParameters</span></span>
<span data-ttu-id="59362-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="59362-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59362-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59362-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59362-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="59362-124">INPUTS</span></span>

### <span data-ttu-id="59362-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="59362-125">None</span></span>
<span data-ttu-id="59362-126">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="59362-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="59362-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="59362-127">OUTPUTS</span></span>

## <span data-ttu-id="59362-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="59362-128">NOTES</span></span>

## <span data-ttu-id="59362-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="59362-129">RELATED LINKS</span></span>

[<span data-ttu-id="59362-130">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="59362-130">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="59362-131">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="59362-131">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)

[<span data-ttu-id="59362-132">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="59362-132">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)


