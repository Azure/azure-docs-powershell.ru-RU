---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 32CF9DA7-5607-4CF9-A2D0-D76A0C005FDA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMAccessExtension.md
ms.openlocfilehash: 889bd206566b9c722aa187f9e32a76c1711af337
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732316"
---
# <span data-ttu-id="97268-101">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="97268-101">Get-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="97268-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="97268-102">SYNOPSIS</span></span>
<span data-ttu-id="97268-103">Получает сведения о расширении VMAccess.</span><span class="sxs-lookup"><span data-stu-id="97268-103">Gets information about the VMAccess extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97268-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="97268-104">SYNTAX</span></span>

```
Get-AzureRmVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97268-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="97268-105">DESCRIPTION</span></span>
<span data-ttu-id="97268-106">Командлет **Get-AzureRmVMAccessExtension** получает сведения о расширении виртуальной машины доступа к виртуальной машине (VMAccess).</span><span class="sxs-lookup"><span data-stu-id="97268-106">The **Get-AzureRmVMAccessExtension** cmdlet gets information about the Virtual Machine Access (VMAccess) Virtual Machine Extension.</span></span>

## <span data-ttu-id="97268-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="97268-107">EXAMPLES</span></span>

### <span data-ttu-id="97268-108">Пример 1: получение расширения VMAccess</span><span class="sxs-lookup"><span data-stu-id="97268-108">Example 1: Get the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzureRmVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest"
```

<span data-ttu-id="97268-109">Эта команда получает расширение VMAccess с именем ContosoTest для виртуальной машины с именем VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="97268-109">This command gets the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="97268-110">Пример 2: получение представления экземпляра расширения VMAccess</span><span class="sxs-lookup"><span data-stu-id="97268-110">Example 2: Get the instance view of the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzureRmVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest" -Status
```

<span data-ttu-id="97268-111">Эта команда получает представление экземпляра расширения VMAccess с именем ContosoTest для виртуальной машины с именем VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="97268-111">This command gets the instance view of the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="97268-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="97268-112">PARAMETERS</span></span>

### <span data-ttu-id="97268-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97268-113">-DefaultProfile</span></span>
<span data-ttu-id="97268-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="97268-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97268-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="97268-115">-Name</span></span>
<span data-ttu-id="97268-116">Указывает имя расширения, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="97268-116">Specifies the name of the extension that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97268-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97268-117">-ResourceGroupName</span></span>
<span data-ttu-id="97268-118">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="97268-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="97268-119">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="97268-119">-Status</span></span>
<span data-ttu-id="97268-120">Указывает на то, что этот командлет получает только представление экземпляра расширения.</span><span class="sxs-lookup"><span data-stu-id="97268-120">Indicates that this cmdlet gets only the instance view of the extension.</span></span>

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

### <span data-ttu-id="97268-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="97268-121">-VMName</span></span>
<span data-ttu-id="97268-122">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="97268-122">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="97268-123">Этот командлет получает сведения о VMAccess для виртуальной машины, указывающей этот параметр.</span><span class="sxs-lookup"><span data-stu-id="97268-123">This cmdlet gets information about VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="97268-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97268-124">CommonParameters</span></span>
<span data-ttu-id="97268-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="97268-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97268-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97268-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97268-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="97268-127">INPUTS</span></span>

### <span data-ttu-id="97268-128">System. String</span><span class="sxs-lookup"><span data-stu-id="97268-128">System.String</span></span>

### <span data-ttu-id="97268-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="97268-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="97268-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="97268-130">OUTPUTS</span></span>

### <span data-ttu-id="97268-131">Microsoft. Azure. Commands. COMPUTE. Models. VirtualMachineAccessExtensionContext</span><span class="sxs-lookup"><span data-stu-id="97268-131">Microsoft.Azure.Commands.Compute.Models.VirtualMachineAccessExtensionContext</span></span>

## <span data-ttu-id="97268-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="97268-132">NOTES</span></span>

## <span data-ttu-id="97268-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="97268-133">RELATED LINKS</span></span>

[<span data-ttu-id="97268-134">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="97268-134">Remove-AzureRmVMAccessExtension</span></span>](./Remove-AzureRmVMAccessExtension.md)

[<span data-ttu-id="97268-135">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="97268-135">Set-AzureRmVMAccessExtension</span></span>](./Set-AzureRmVMAccessExtension.md)

[<span data-ttu-id="97268-136">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="97268-136">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)


