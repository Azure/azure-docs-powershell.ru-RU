---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 5B7A1BE6-F5F5-4968-BE32-7743D0E25FE3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDscExtension.md
ms.openlocfilehash: 0a3c54331b557b6be279ab5ce3f9fafad62b158c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559216"
---
# <span data-ttu-id="c6b67-101">Get-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="c6b67-101">Get-AzureRmVMDscExtension</span></span>

## <span data-ttu-id="c6b67-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c6b67-102">SYNOPSIS</span></span>
<span data-ttu-id="c6b67-103">Получает параметры расширения DSC для определенной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c6b67-103">Gets the settings of the DSC extension on a particular virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6b67-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c6b67-104">SYNTAX</span></span>

```
Get-AzureRmVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [<CommonParameters>]
```

## <span data-ttu-id="c6b67-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c6b67-105">DESCRIPTION</span></span>
<span data-ttu-id="c6b67-106">Командлет **Get-AzureRmVMDscExtension** получает параметры расширения конфигурации нужного состояния (DSC) на определенной виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="c6b67-106">The **Get-AzureRmVMDscExtension** cmdlet gets the settings of the Desired State Configuration (DSC) extension on a particular virtual machine.</span></span>

## <span data-ttu-id="c6b67-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c6b67-107">EXAMPLES</span></span>

### <span data-ttu-id="c6b67-108">Пример 1: получение параметров расширения DSC</span><span class="sxs-lookup"><span data-stu-id="c6b67-108">Example 1: Get the settings of a DSC extension</span></span>
```
PS C:\> Get-AzureRmVMDscExtension -ResourceGroupName "ResourceGroup002" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="c6b67-109">Эта команда получает параметры расширения с именем DSC на виртуальной машине с именем VM07.</span><span class="sxs-lookup"><span data-stu-id="c6b67-109">This command gets the settings of extension named DSC on the virtual machine named VM07.</span></span>

## <span data-ttu-id="c6b67-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c6b67-110">PARAMETERS</span></span>

### <span data-ttu-id="c6b67-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c6b67-111">-Name</span></span>
<span data-ttu-id="c6b67-112">Указывает имя ресурса диспетчера ресурсов Azure, представляющего расширение.</span><span class="sxs-lookup"><span data-stu-id="c6b67-112">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="c6b67-113">Командлет Set-AzureRmVMDscExtension задает для этого имени имя Microsoft. PowerShell. DSC, которое совпадает со значением, которое используется для **Get-AzureRmVMDscExtension**.</span><span class="sxs-lookup"><span data-stu-id="c6b67-113">The Set-AzureRmVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzureRmVMDscExtension**.</span></span>
<span data-ttu-id="c6b67-114">Указывайте этот параметр только в том случае, если вы изменили имя по умолчанию в командлете **Set-AzureRmVMDscExtension** или использовали другое имя ресурса в шаблоне диспетчера ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c6b67-114">Specify this parameter only if you changed the default name in the **Set-AzureRmVMDscExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

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

### <span data-ttu-id="c6b67-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6b67-115">-ResourceGroupName</span></span>
<span data-ttu-id="c6b67-116">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c6b67-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="c6b67-117">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="c6b67-117">-Status</span></span>
<span data-ttu-id="c6b67-118">Указывает на то, что этот командлет получает представление экземпляра расширения DSC.</span><span class="sxs-lookup"><span data-stu-id="c6b67-118">Indicates that this cmdlet gets the instance view of the DSC extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6b67-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="c6b67-119">-VMName</span></span>
<span data-ttu-id="c6b67-120">Указывает имя виртуальной машины, для которой этот командлет получает расширение DSC.</span><span class="sxs-lookup"><span data-stu-id="c6b67-120">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension.</span></span>

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

### <span data-ttu-id="c6b67-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6b67-121">CommonParameters</span></span>
<span data-ttu-id="c6b67-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c6b67-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6b67-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6b67-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6b67-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c6b67-124">INPUTS</span></span>

### <span data-ttu-id="c6b67-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="c6b67-125">None</span></span>
<span data-ttu-id="c6b67-126">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="c6b67-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c6b67-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c6b67-127">OUTPUTS</span></span>

### <span data-ttu-id="c6b67-128">Microsoft. Azure. Commands. COMPUTE. extension. DSC. VirtualMachineDscExtensionContext</span><span class="sxs-lookup"><span data-stu-id="c6b67-128">Microsoft.Azure.Commands.Compute.Extension.DSC.VirtualMachineDscExtensionContext</span></span>

## <span data-ttu-id="c6b67-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="c6b67-129">NOTES</span></span>

## <span data-ttu-id="c6b67-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c6b67-130">RELATED LINKS</span></span>

[<span data-ttu-id="c6b67-131">Remove-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="c6b67-131">Remove-AzureRmVMDscExtension</span></span>](./Remove-AzureRmVMDscExtension.md)

[<span data-ttu-id="c6b67-132">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="c6b67-132">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)


