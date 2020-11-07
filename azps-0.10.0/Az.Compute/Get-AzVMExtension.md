---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 842652D4-0F1C-4D0D-AB55-0D43D3C5D82A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMExtension.md
ms.openlocfilehash: a8ac31efd77d5b8ff5c07920bb14b44f80ac0955
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911527"
---
# <span data-ttu-id="a09dd-101">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="a09dd-101">Get-AzVMExtension</span></span>

## <span data-ttu-id="a09dd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a09dd-102">SYNOPSIS</span></span>
<span data-ttu-id="a09dd-103">Возвращает свойства расширений виртуальных машин, установленных на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="a09dd-103">Gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>

## <span data-ttu-id="a09dd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a09dd-104">SYNTAX</span></span>

```
Get-AzVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a09dd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a09dd-105">DESCRIPTION</span></span>
<span data-ttu-id="a09dd-106">Командлет **Get-AzVMExtension** получает свойства расширений виртуальных машин, установленных на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="a09dd-106">The **Get-AzVMExtension** cmdlet gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>
<span data-ttu-id="a09dd-107">Укажите имя расширения, для которого нужно получить свойства.</span><span class="sxs-lookup"><span data-stu-id="a09dd-107">Specify the name of an extension for which to get properties.</span></span>
<span data-ttu-id="a09dd-108">Чтобы получить только представление экземпляра расширения, укажите параметр Status.</span><span class="sxs-lookup"><span data-stu-id="a09dd-108">To get only the instance view of an extension, specify the Status parameter.</span></span>

## <span data-ttu-id="a09dd-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a09dd-109">EXAMPLES</span></span>

### <span data-ttu-id="a09dd-110">Пример 1: получение свойств расширения</span><span class="sxs-lookup"><span data-stu-id="a09dd-110">Example 1: Get properties of an extension</span></span>
```
PS C:\> Get-AzVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension"
```

<span data-ttu-id="a09dd-111">Эта команда получает свойства для расширения с именем CustomScriptExtension на виртуальной машине с именем VirtualMachine22 в группе ресурсов ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="a09dd-111">This command gets properties for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="a09dd-112">Пример 2: получение представления экземпляра расширения</span><span class="sxs-lookup"><span data-stu-id="a09dd-112">Example 2: Get instance view of an extension</span></span>
```
PS C:\> Get-AzVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Status
```

<span data-ttu-id="a09dd-113">Эта команда получает представление экземпляра для расширения с именем CustomScriptExtension на виртуальной машине с именем VirtualMachine22 в группе ресурсов ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="a09dd-113">This command gets the instance view for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="a09dd-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a09dd-114">PARAMETERS</span></span>

### <span data-ttu-id="a09dd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a09dd-115">-DefaultProfile</span></span>
<span data-ttu-id="a09dd-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a09dd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a09dd-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a09dd-117">-Name</span></span>
<span data-ttu-id="a09dd-118">Указывает имя расширения.</span><span class="sxs-lookup"><span data-stu-id="a09dd-118">Specifies the name of an extension.</span></span>
<span data-ttu-id="a09dd-119">Этот командлет получает свойства для расширения, которое указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="a09dd-119">This cmdlet gets properties for the extension that this parameter specifies.</span></span>

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

### <span data-ttu-id="a09dd-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a09dd-120">-ResourceGroupName</span></span>
<span data-ttu-id="a09dd-121">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a09dd-121">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="a09dd-122">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="a09dd-122">-Status</span></span>
<span data-ttu-id="a09dd-123">Указывает на то, что этот командлет получает только представление экземпляра расширения.</span><span class="sxs-lookup"><span data-stu-id="a09dd-123">Indicates that this cmdlet gets only the instance view of an extension.</span></span>

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

### <span data-ttu-id="a09dd-124">-VMName</span><span class="sxs-lookup"><span data-stu-id="a09dd-124">-VMName</span></span>
<span data-ttu-id="a09dd-125">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a09dd-125">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="a09dd-126">Этот командлет получает свойства расширения из виртуальной машины, указывающей этот параметр.</span><span class="sxs-lookup"><span data-stu-id="a09dd-126">This cmdlet gets properties of an extension from the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="a09dd-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a09dd-127">CommonParameters</span></span>
<span data-ttu-id="a09dd-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a09dd-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a09dd-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a09dd-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a09dd-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a09dd-130">INPUTS</span></span>

### <span data-ttu-id="a09dd-131">Ничего</span><span class="sxs-lookup"><span data-stu-id="a09dd-131">None</span></span>
<span data-ttu-id="a09dd-132">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="a09dd-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a09dd-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a09dd-133">OUTPUTS</span></span>

### <span data-ttu-id="a09dd-134">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="a09dd-134">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="a09dd-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="a09dd-135">NOTES</span></span>

## <span data-ttu-id="a09dd-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a09dd-136">RELATED LINKS</span></span>

[<span data-ttu-id="a09dd-137">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="a09dd-137">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)

[<span data-ttu-id="a09dd-138">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="a09dd-138">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)


