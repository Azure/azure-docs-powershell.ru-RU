---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6C40A7BA-6BE2-464A-84E4-9021935A5BF6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmextension
schema: 2.0.0
ms.openlocfilehash: 835413728b22dd8bbb80d472eed71e0f4185db89
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914205"
---
# <span data-ttu-id="626ee-101">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="626ee-101">Remove-AzureRmVMExtension</span></span>

## <span data-ttu-id="626ee-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="626ee-102">SYNOPSIS</span></span>
<span data-ttu-id="626ee-103">Удаляет расширение из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="626ee-103">Removes an extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="626ee-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="626ee-104">SYNTAX</span></span>

```
Remove-AzureRmVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="626ee-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="626ee-105">DESCRIPTION</span></span>
<span data-ttu-id="626ee-106">Командлет **Remove-AzureRmVMExtension** удаляет расширение из расширений виртуальных машин виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="626ee-106">The **Remove-AzureRmVMExtension** cmdlet removes an extension from the Virtual Machine Extensions of a virtual machine.</span></span>

## <span data-ttu-id="626ee-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="626ee-107">EXAMPLES</span></span>

### <span data-ttu-id="626ee-108">Пример 1: удаление расширения из виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="626ee-108">Example 1: Remove an extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -Name "ContosoTest" -VMName "VirtualMachine22"
```

<span data-ttu-id="626ee-109">Эта команда удаляет расширение ContosoTest с виртуальной машины с именем VirtualMachine22 в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="626ee-109">This command removes the extension named ContosoTest from the virtual machine named VirtualMachine22 in ResourceGroup11.</span></span>

## <span data-ttu-id="626ee-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="626ee-110">PARAMETERS</span></span>

### <span data-ttu-id="626ee-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="626ee-111">-DefaultProfile</span></span>
<span data-ttu-id="626ee-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="626ee-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="626ee-113">-Force</span><span class="sxs-lookup"><span data-stu-id="626ee-113">-Force</span></span>
<span data-ttu-id="626ee-114">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="626ee-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="626ee-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="626ee-115">-Name</span></span>
<span data-ttu-id="626ee-116">Указывает имя расширения, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="626ee-116">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="626ee-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="626ee-117">-ResourceGroupName</span></span>
<span data-ttu-id="626ee-118">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="626ee-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="626ee-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="626ee-119">-VMName</span></span>
<span data-ttu-id="626ee-120">Указывает имя виртуальной машины, с помощью которой этот командлет удаляет расширение.</span><span class="sxs-lookup"><span data-stu-id="626ee-120">Specifies the name of a virtual machine from which this cmdlet removes the extension.</span></span>

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

### <span data-ttu-id="626ee-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="626ee-121">-Confirm</span></span>
<span data-ttu-id="626ee-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="626ee-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="626ee-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="626ee-123">-WhatIf</span></span>
<span data-ttu-id="626ee-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="626ee-124">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="626ee-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="626ee-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="626ee-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="626ee-126">CommonParameters</span></span>
<span data-ttu-id="626ee-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="626ee-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="626ee-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="626ee-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="626ee-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="626ee-129">INPUTS</span></span>

### <span data-ttu-id="626ee-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="626ee-130">None</span></span>
<span data-ttu-id="626ee-131">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="626ee-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="626ee-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="626ee-132">OUTPUTS</span></span>

### <span data-ttu-id="626ee-133">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="626ee-133">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="626ee-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="626ee-134">NOTES</span></span>

## <span data-ttu-id="626ee-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="626ee-135">RELATED LINKS</span></span>

[<span data-ttu-id="626ee-136">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="626ee-136">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)

[<span data-ttu-id="626ee-137">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="626ee-137">Set-AzureRmVMExtension</span></span>](./Set-AzureRmVMExtension.md)


