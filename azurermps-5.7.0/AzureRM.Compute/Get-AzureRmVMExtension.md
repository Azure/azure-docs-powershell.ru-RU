---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 842652D4-0F1C-4D0D-AB55-0D43D3C5D82A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtension.md
ms.openlocfilehash: 82ab2f02d47b17342f71b09eebe826fc48c07b81
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559208"
---
# <span data-ttu-id="f4cb6-101">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="f4cb6-101">Get-AzureRmVMExtension</span></span>

## <span data-ttu-id="f4cb6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f4cb6-102">SYNOPSIS</span></span>
<span data-ttu-id="f4cb6-103">Возвращает свойства расширений виртуальных машин, установленных на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="f4cb6-103">Gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4cb6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f4cb6-104">SYNTAX</span></span>

```
Get-AzureRmVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [<CommonParameters>]
```

## <span data-ttu-id="f4cb6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4cb6-105">DESCRIPTION</span></span>
<span data-ttu-id="f4cb6-106">Командлет **Get-AzureRmVMExtension** получает свойства расширений виртуальных машин, установленных на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="f4cb6-106">The **Get-AzureRmVMExtension** cmdlet gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>
<span data-ttu-id="f4cb6-107">Укажите имя расширения, для которого нужно получить свойства.</span><span class="sxs-lookup"><span data-stu-id="f4cb6-107">Specify the name of an extension for which to get properties.</span></span>
<span data-ttu-id="f4cb6-108">Чтобы получить только представление экземпляра расширения, укажите параметр Status.</span><span class="sxs-lookup"><span data-stu-id="f4cb6-108">To get only the instance view of an extension, specify the Status parameter.</span></span>

## <span data-ttu-id="f4cb6-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f4cb6-109">EXAMPLES</span></span>

### <span data-ttu-id="f4cb6-110">Пример 1: получение свойств расширения</span><span class="sxs-lookup"><span data-stu-id="f4cb6-110">Example 1: Get properties of an extension</span></span>
```
PS C:\> Get-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension"
```

<span data-ttu-id="f4cb6-111">Эта команда получает свойства для расширения с именем CustomScriptExtension на виртуальной машине с именем VirtualMachine22 в группе ресурсов ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="f4cb6-111">This command gets properties for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="f4cb6-112">Пример 2: получение представления экземпляра расширения</span><span class="sxs-lookup"><span data-stu-id="f4cb6-112">Example 2: Get instance view of an extension</span></span>
```
PS C:\> Get-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Status
```

<span data-ttu-id="f4cb6-113">Эта команда получает представление экземпляра для расширения с именем CustomScriptExtension на виртуальной машине с именем VirtualMachine22 в группе ресурсов ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="f4cb6-113">This command gets the instance view for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="f4cb6-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f4cb6-114">PARAMETERS</span></span>

### <span data-ttu-id="f4cb6-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f4cb6-115">-Name</span></span>
<span data-ttu-id="f4cb6-116">Указывает имя расширения.</span><span class="sxs-lookup"><span data-stu-id="f4cb6-116">Specifies the name of an extension.</span></span>
<span data-ttu-id="f4cb6-117">Этот командлет получает свойства для расширения, которое указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="f4cb6-117">This cmdlet gets properties for the extension that this parameter specifies.</span></span>

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

### <span data-ttu-id="f4cb6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4cb6-118">-ResourceGroupName</span></span>
<span data-ttu-id="f4cb6-119">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f4cb6-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f4cb6-120">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="f4cb6-120">-Status</span></span>
<span data-ttu-id="f4cb6-121">Указывает на то, что этот командлет получает только представление экземпляра расширения.</span><span class="sxs-lookup"><span data-stu-id="f4cb6-121">Indicates that this cmdlet gets only the instance view of an extension.</span></span>

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

### <span data-ttu-id="f4cb6-122">-VMName</span><span class="sxs-lookup"><span data-stu-id="f4cb6-122">-VMName</span></span>
<span data-ttu-id="f4cb6-123">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f4cb6-123">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="f4cb6-124">Этот командлет получает свойства расширения из виртуальной машины, указывающей этот параметр.</span><span class="sxs-lookup"><span data-stu-id="f4cb6-124">This cmdlet gets properties of an extension from the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="f4cb6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4cb6-125">CommonParameters</span></span>
<span data-ttu-id="f4cb6-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f4cb6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4cb6-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4cb6-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4cb6-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f4cb6-128">INPUTS</span></span>

### <span data-ttu-id="f4cb6-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="f4cb6-129">None</span></span>
<span data-ttu-id="f4cb6-130">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="f4cb6-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f4cb6-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4cb6-131">OUTPUTS</span></span>

## <span data-ttu-id="f4cb6-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="f4cb6-132">NOTES</span></span>

## <span data-ttu-id="f4cb6-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f4cb6-133">RELATED LINKS</span></span>

[<span data-ttu-id="f4cb6-134">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="f4cb6-134">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)

[<span data-ttu-id="f4cb6-135">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="f4cb6-135">Set-AzureRmVMExtension</span></span>](./Set-AzureRmVMExtension.md)


