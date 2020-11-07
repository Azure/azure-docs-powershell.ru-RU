---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 32CF9DA7-5607-4CF9-A2D0-D76A0C005FDA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmaccessextension
schema: 2.0.0
ms.openlocfilehash: 5d07d90e7a9902713be3ef4d2acf3a2650e4f1b4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913676"
---
# <span data-ttu-id="8a660-101">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="8a660-101">Get-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="8a660-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8a660-102">SYNOPSIS</span></span>
<span data-ttu-id="8a660-103">Получает сведения о расширении VMAccess.</span><span class="sxs-lookup"><span data-stu-id="8a660-103">Gets information about the VMAccess extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a660-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8a660-104">SYNTAX</span></span>

```
Get-AzureRmVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a660-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a660-105">DESCRIPTION</span></span>
<span data-ttu-id="8a660-106">Командлет **Get-AzureRmVMAccessExtension** получает сведения о расширении виртуальной машины доступа к виртуальной машине (VMAccess).</span><span class="sxs-lookup"><span data-stu-id="8a660-106">The **Get-AzureRmVMAccessExtension** cmdlet gets information about the Virtual Machine Access (VMAccess) Virtual Machine Extension.</span></span>

## <span data-ttu-id="8a660-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8a660-107">EXAMPLES</span></span>

### <span data-ttu-id="8a660-108">Пример 1: получение расширения VMAccess</span><span class="sxs-lookup"><span data-stu-id="8a660-108">Example 1: Get the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzureRmVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest"
```

<span data-ttu-id="8a660-109">Эта команда получает расширение VMAccess с именем ContosoTest для виртуальной машины с именем VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="8a660-109">This command gets the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="8a660-110">Пример 2: получение представления экземпляра расширения VMAccess</span><span class="sxs-lookup"><span data-stu-id="8a660-110">Example 2: Get the instance view of the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzureRmVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest" -Status
```

<span data-ttu-id="8a660-111">Эта команда получает представление экземпляра расширения VMAccess с именем ContosoTest для виртуальной машины с именем VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="8a660-111">This command gets the instance view of the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="8a660-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8a660-112">PARAMETERS</span></span>

### <span data-ttu-id="8a660-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a660-113">-DefaultProfile</span></span>
<span data-ttu-id="8a660-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8a660-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a660-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8a660-115">-Name</span></span>
<span data-ttu-id="8a660-116">Указывает имя расширения, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="8a660-116">Specifies the name of the extension that this cmdlet gets.</span></span>

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

### <span data-ttu-id="8a660-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a660-117">-ResourceGroupName</span></span>
<span data-ttu-id="8a660-118">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="8a660-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="8a660-119">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="8a660-119">-Status</span></span>
<span data-ttu-id="8a660-120">Указывает на то, что этот командлет получает только представление экземпляра расширения.</span><span class="sxs-lookup"><span data-stu-id="8a660-120">Indicates that this cmdlet gets only the instance view of the extension.</span></span>

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

### <span data-ttu-id="8a660-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="8a660-121">-VMName</span></span>
<span data-ttu-id="8a660-122">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="8a660-122">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="8a660-123">Этот командлет получает сведения о VMAccess для виртуальной машины, указывающей этот параметр.</span><span class="sxs-lookup"><span data-stu-id="8a660-123">This cmdlet gets information about VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="8a660-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a660-124">CommonParameters</span></span>
<span data-ttu-id="8a660-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8a660-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a660-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a660-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a660-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8a660-127">INPUTS</span></span>

### <span data-ttu-id="8a660-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="8a660-128">None</span></span>
<span data-ttu-id="8a660-129">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="8a660-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8a660-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a660-130">OUTPUTS</span></span>

### <span data-ttu-id="8a660-131">Microsoft. Azure. Commands. COMPUTE. Models. VirtualMachineAccessExtensionContext</span><span class="sxs-lookup"><span data-stu-id="8a660-131">Microsoft.Azure.Commands.Compute.Models.VirtualMachineAccessExtensionContext</span></span>

## <span data-ttu-id="8a660-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="8a660-132">NOTES</span></span>

## <span data-ttu-id="8a660-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8a660-133">RELATED LINKS</span></span>

[<span data-ttu-id="8a660-134">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="8a660-134">Remove-AzureRmVMAccessExtension</span></span>](./Remove-AzureRmVMAccessExtension.md)

[<span data-ttu-id="8a660-135">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="8a660-135">Set-AzureRmVMAccessExtension</span></span>](./Set-AzureRmVMAccessExtension.md)

[<span data-ttu-id="8a660-136">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="8a660-136">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)


