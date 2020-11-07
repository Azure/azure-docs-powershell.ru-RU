---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: C7FCF2CA-2C8D-4280-BF68-10DEA96642A5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmdscextension
schema: 2.0.0
ms.openlocfilehash: f93d461bddb78230be3168cb1df534a4cde842e2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914209"
---
# <span data-ttu-id="7c479-101">Remove-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="7c479-101">Remove-AzureRmVMDscExtension</span></span>

## <span data-ttu-id="7c479-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7c479-102">SYNOPSIS</span></span>
<span data-ttu-id="7c479-103">Удаляет обработчик расширений DSC из виртуальной машины в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7c479-103">Removes a DSC extension handler from a virtual machine in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c479-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7c479-104">SYNTAX</span></span>

```
Remove-AzureRmVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c479-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7c479-105">DESCRIPTION</span></span>
<span data-ttu-id="7c479-106">Командлет **Remove-AzureRmVMDscExtension** удаляет обработчик расширения нужной конфигурации состояния (DSC) из виртуальной машины в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7c479-106">The **Remove-AzureRmVMDscExtension** cmdlet removes a Desired State Configuration (DSC) extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="7c479-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7c479-107">EXAMPLES</span></span>

### <span data-ttu-id="7c479-108">Пример 1: удаление расширения DSC</span><span class="sxs-lookup"><span data-stu-id="7c479-108">Example 1: Remove a DSC extension</span></span>
```
PS C:\> Remove-AzureRmVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="7c479-109">Эта команда удаляет расширение с именем DSC на виртуальной машине с именем VM07.</span><span class="sxs-lookup"><span data-stu-id="7c479-109">This command removes the extension named DSC on virtual machine named VM07.</span></span>

## <span data-ttu-id="7c479-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7c479-110">PARAMETERS</span></span>

### <span data-ttu-id="7c479-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c479-111">-DefaultProfile</span></span>
<span data-ttu-id="7c479-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7c479-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c479-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7c479-113">-Name</span></span>
<span data-ttu-id="7c479-114">Указывает имя расширения DSC, которое удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="7c479-114">Specifies the name of the DSC extension that this cmdlet removes.</span></span>
<span data-ttu-id="7c479-115">Командлет Set-AzureRmVMDscExtension задает это имя в Microsoft. PowerShell. DSC, которое является значением по умолчанию, используемым функцией **Remove-AzureRmVMDscExtension**.</span><span class="sxs-lookup"><span data-stu-id="7c479-115">The Set-AzureRmVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the default value used by **Remove-AzureRmVMDscExtension**.</span></span>

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

### <span data-ttu-id="7c479-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c479-116">-ResourceGroupName</span></span>
<span data-ttu-id="7c479-117">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="7c479-117">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="7c479-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="7c479-118">-VMName</span></span>
<span data-ttu-id="7c479-119">Указывает имя виртуальной машины, с помощью которой этот командлет удаляет расширение DSC.</span><span class="sxs-lookup"><span data-stu-id="7c479-119">Specifies the name of a virtual machine from which this cmdlet removes the DSC extension.</span></span>

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

### <span data-ttu-id="7c479-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7c479-120">-Confirm</span></span>
<span data-ttu-id="7c479-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7c479-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c479-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c479-122">-WhatIf</span></span>
<span data-ttu-id="7c479-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7c479-123">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="7c479-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7c479-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c479-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c479-125">CommonParameters</span></span>
<span data-ttu-id="7c479-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7c479-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c479-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c479-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c479-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7c479-128">INPUTS</span></span>

### <span data-ttu-id="7c479-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="7c479-129">None</span></span>
<span data-ttu-id="7c479-130">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="7c479-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7c479-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7c479-131">OUTPUTS</span></span>

### <span data-ttu-id="7c479-132">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="7c479-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="7c479-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="7c479-133">NOTES</span></span>

## <span data-ttu-id="7c479-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7c479-134">RELATED LINKS</span></span>

[<span data-ttu-id="7c479-135">Get-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="7c479-135">Get-AzureRmVMDscExtension</span></span>](./Get-AzureRmVMDscExtension.md)

[<span data-ttu-id="7c479-136">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="7c479-136">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)


