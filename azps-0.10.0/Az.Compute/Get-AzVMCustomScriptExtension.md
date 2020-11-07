---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 1017A74D-6420-4E51-A4A4-1AD3AD6D8122
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMCustomScriptExtension.md
ms.openlocfilehash: 0639907999b3e84f5f609a3f0c6f1063204438ca
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911537"
---
# <span data-ttu-id="f0179-101">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="f0179-101">Get-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="f0179-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f0179-102">SYNOPSIS</span></span>
<span data-ttu-id="f0179-103">Получает сведения о настраиваемом расширении сценария.</span><span class="sxs-lookup"><span data-stu-id="f0179-103">Gets information about a custom script extension.</span></span>

## <span data-ttu-id="f0179-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f0179-104">SYNTAX</span></span>

```
Get-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0179-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0179-105">DESCRIPTION</span></span>
<span data-ttu-id="f0179-106">Командлет **Get-AzVMCustomScriptExtension** получает сведения о расширении виртуальной машины настраиваемого сценария на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="f0179-106">The **Get-AzVMCustomScriptExtension** cmdlet gets information about a custom script Virtual Machine Extension on a virtual machine.</span></span>

## <span data-ttu-id="f0179-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f0179-107">EXAMPLES</span></span>

### <span data-ttu-id="f0179-108">Пример 1: получение расширения настраиваемого сценария</span><span class="sxs-lookup"><span data-stu-id="f0179-108">Example 1: Get a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript"
```

<span data-ttu-id="f0179-109">Эта команда получает настраиваемое расширение сценария с именем ContosoCustomScript для виртуальной машины с именем VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="f0179-109">This command gets the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="f0179-110">Пример 2: получение представления экземпляра настраиваемого расширения сценария</span><span class="sxs-lookup"><span data-stu-id="f0179-110">Example 2: Get the instance view of a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript" -Status
```

<span data-ttu-id="f0179-111">Эта команда получает представление экземпляра настраиваемого расширения сценария с именем ContosoCustomScript для виртуальной машины с именем VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="f0179-111">This command gets the instance view of the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="f0179-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f0179-112">PARAMETERS</span></span>

### <span data-ttu-id="f0179-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0179-113">-DefaultProfile</span></span>
<span data-ttu-id="f0179-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f0179-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0179-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f0179-115">-Name</span></span>
<span data-ttu-id="f0179-116">Указывает имя настраиваемого расширения сценария, для которого этот командлет получает сведения.</span><span class="sxs-lookup"><span data-stu-id="f0179-116">Specifies the name of the custom script extension about which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="f0179-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0179-117">-ResourceGroupName</span></span>
<span data-ttu-id="f0179-118">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f0179-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="f0179-119">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="f0179-119">-Status</span></span>
<span data-ttu-id="f0179-120">Указывает на то, что этот командлет получает представление экземпляра для расширения настраиваемого сценария.</span><span class="sxs-lookup"><span data-stu-id="f0179-120">Indicates that this cmdlet gets the instance view of the custom script extension.</span></span>

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

### <span data-ttu-id="f0179-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="f0179-121">-VMName</span></span>
<span data-ttu-id="f0179-122">Указывает имя виртуальной машины, для которой этот командлет получает настраиваемое расширение сценария.</span><span class="sxs-lookup"><span data-stu-id="f0179-122">Specifies the name of a virtual machine for which this cmdlet gets the custom script extension.</span></span>

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

### <span data-ttu-id="f0179-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0179-123">CommonParameters</span></span>
<span data-ttu-id="f0179-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f0179-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0179-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0179-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0179-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f0179-126">INPUTS</span></span>

### <span data-ttu-id="f0179-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="f0179-127">None</span></span>
<span data-ttu-id="f0179-128">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="f0179-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f0179-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0179-129">OUTPUTS</span></span>

### <span data-ttu-id="f0179-130">Microsoft. Azure. Commands. COMPUTE. Models. VirtualMachineCustomScriptExtensionContext</span><span class="sxs-lookup"><span data-stu-id="f0179-130">Microsoft.Azure.Commands.Compute.Models.VirtualMachineCustomScriptExtensionContext</span></span>

## <span data-ttu-id="f0179-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="f0179-131">NOTES</span></span>

## <span data-ttu-id="f0179-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f0179-132">RELATED LINKS</span></span>

[<span data-ttu-id="f0179-133">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="f0179-133">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="f0179-134">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="f0179-134">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="f0179-135">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="f0179-135">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)


