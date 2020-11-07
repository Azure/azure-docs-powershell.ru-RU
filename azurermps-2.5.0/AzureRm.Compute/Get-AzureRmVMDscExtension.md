---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 5B7A1BE6-F5F5-4968-BE32-7743D0E25FE3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmdscextension
schema: 2.0.0
ms.openlocfilehash: 0954bcb395cf4a0dcf64dac178b1168ee1abd59b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913928"
---
# <span data-ttu-id="c7f65-101">Get-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="c7f65-101">Get-AzureRmVMDscExtension</span></span>

## <span data-ttu-id="c7f65-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c7f65-102">SYNOPSIS</span></span>
<span data-ttu-id="c7f65-103">Получает параметры расширения DSC для определенной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c7f65-103">Gets the settings of the DSC extension on a particular virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7f65-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c7f65-104">SYNTAX</span></span>

```
Get-AzureRmVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7f65-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c7f65-105">DESCRIPTION</span></span>
<span data-ttu-id="c7f65-106">Командлет **Get-AzureRmVMDscExtension** получает параметры расширения конфигурации нужного состояния (DSC) на определенной виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="c7f65-106">The **Get-AzureRmVMDscExtension** cmdlet gets the settings of the Desired State Configuration (DSC) extension on a particular virtual machine.</span></span>

## <span data-ttu-id="c7f65-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c7f65-107">EXAMPLES</span></span>

### <span data-ttu-id="c7f65-108">Пример 1: получение параметров расширения DSC</span><span class="sxs-lookup"><span data-stu-id="c7f65-108">Example 1: Get the settings of a DSC extension</span></span>
```
PS C:\> Get-AzureRmVMDscExtension -ResourceGroupName "ResourceGroup002" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="c7f65-109">Эта команда получает параметры расширения с именем DSC на виртуальной машине с именем VM07.</span><span class="sxs-lookup"><span data-stu-id="c7f65-109">This command gets the settings of extension named DSC on the virtual machine named VM07.</span></span>

## <span data-ttu-id="c7f65-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c7f65-110">PARAMETERS</span></span>

### <span data-ttu-id="c7f65-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7f65-111">-DefaultProfile</span></span>
<span data-ttu-id="c7f65-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c7f65-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7f65-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c7f65-113">-Name</span></span>
<span data-ttu-id="c7f65-114">Указывает имя ресурса диспетчера ресурсов Azure, представляющего расширение.</span><span class="sxs-lookup"><span data-stu-id="c7f65-114">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="c7f65-115">Командлет Set-AzureRmVMDscExtension задает для этого имени имя Microsoft. PowerShell. DSC, которое совпадает со значением, которое используется для **Get-AzureRmVMDscExtension**.</span><span class="sxs-lookup"><span data-stu-id="c7f65-115">The Set-AzureRmVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzureRmVMDscExtension**.</span></span>
<span data-ttu-id="c7f65-116">Указывайте этот параметр только в том случае, если вы изменили имя по умолчанию в командлете **Set-AzureRmVMDscExtension** или использовали другое имя ресурса в шаблоне диспетчера ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c7f65-116">Specify this parameter only if you changed the default name in the **Set-AzureRmVMDscExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

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

### <span data-ttu-id="c7f65-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7f65-117">-ResourceGroupName</span></span>
<span data-ttu-id="c7f65-118">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c7f65-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="c7f65-119">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="c7f65-119">-Status</span></span>
<span data-ttu-id="c7f65-120">Указывает на то, что этот командлет получает представление экземпляра расширения DSC.</span><span class="sxs-lookup"><span data-stu-id="c7f65-120">Indicates that this cmdlet gets the instance view of the DSC extension.</span></span>

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

### <span data-ttu-id="c7f65-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="c7f65-121">-VMName</span></span>
<span data-ttu-id="c7f65-122">Указывает имя виртуальной машины, для которой этот командлет получает расширение DSC.</span><span class="sxs-lookup"><span data-stu-id="c7f65-122">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension.</span></span>

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

### <span data-ttu-id="c7f65-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7f65-123">CommonParameters</span></span>
<span data-ttu-id="c7f65-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c7f65-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7f65-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7f65-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7f65-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c7f65-126">INPUTS</span></span>

### <span data-ttu-id="c7f65-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="c7f65-127">None</span></span>
<span data-ttu-id="c7f65-128">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="c7f65-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c7f65-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c7f65-129">OUTPUTS</span></span>

### <span data-ttu-id="c7f65-130">Microsoft. Azure. Commands. COMPUTE. extension. DSC. VirtualMachineDscExtensionContext</span><span class="sxs-lookup"><span data-stu-id="c7f65-130">Microsoft.Azure.Commands.Compute.Extension.DSC.VirtualMachineDscExtensionContext</span></span>

## <span data-ttu-id="c7f65-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="c7f65-131">NOTES</span></span>

## <span data-ttu-id="c7f65-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c7f65-132">RELATED LINKS</span></span>

[<span data-ttu-id="c7f65-133">Remove-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="c7f65-133">Remove-AzureRmVMDscExtension</span></span>](./Remove-AzureRmVMDscExtension.md)

[<span data-ttu-id="c7f65-134">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="c7f65-134">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)


