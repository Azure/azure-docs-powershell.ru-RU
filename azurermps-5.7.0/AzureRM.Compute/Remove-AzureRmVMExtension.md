---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 6C40A7BA-6BE2-464A-84E4-9021935A5BF6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMExtension.md
ms.openlocfilehash: da05148a0e27ba553f80fa18b44cb45decf9f1df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557536"
---
# <span data-ttu-id="6d841-101">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="6d841-101">Remove-AzureRmVMExtension</span></span>

## <span data-ttu-id="6d841-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6d841-102">SYNOPSIS</span></span>
<span data-ttu-id="6d841-103">Удаляет расширение из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6d841-103">Removes an extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d841-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6d841-104">SYNTAX</span></span>

```
Remove-AzureRmVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d841-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d841-105">DESCRIPTION</span></span>
<span data-ttu-id="6d841-106">Командлет **Remove-AzureRmVMExtension** удаляет расширение из расширений виртуальных машин виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6d841-106">The **Remove-AzureRmVMExtension** cmdlet removes an extension from the Virtual Machine Extensions of a virtual machine.</span></span>

## <span data-ttu-id="6d841-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6d841-107">EXAMPLES</span></span>

### <span data-ttu-id="6d841-108">Пример 1: удаление расширения из виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="6d841-108">Example 1: Remove an extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -Name "ContosoTest" -VMName "VirtualMachine22"
```

<span data-ttu-id="6d841-109">Эта команда удаляет расширение ContosoTest с виртуальной машины с именем VirtualMachine22 в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="6d841-109">This command removes the extension named ContosoTest from the virtual machine named VirtualMachine22 in ResourceGroup11.</span></span>

## <span data-ttu-id="6d841-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6d841-110">PARAMETERS</span></span>

### <span data-ttu-id="6d841-111">-Force</span><span class="sxs-lookup"><span data-stu-id="6d841-111">-Force</span></span>
<span data-ttu-id="6d841-112">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="6d841-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6d841-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6d841-113">-Name</span></span>
<span data-ttu-id="6d841-114">Указывает имя расширения, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="6d841-114">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6d841-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d841-115">-ResourceGroupName</span></span>
<span data-ttu-id="6d841-116">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6d841-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="6d841-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="6d841-117">-VMName</span></span>
<span data-ttu-id="6d841-118">Указывает имя виртуальной машины, с помощью которой этот командлет удаляет расширение.</span><span class="sxs-lookup"><span data-stu-id="6d841-118">Specifies the name of a virtual machine from which this cmdlet removes the extension.</span></span>

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

### <span data-ttu-id="6d841-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6d841-119">-Confirm</span></span>
<span data-ttu-id="6d841-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6d841-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d841-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d841-121">-WhatIf</span></span>
<span data-ttu-id="6d841-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6d841-122">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="6d841-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6d841-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d841-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d841-124">CommonParameters</span></span>
<span data-ttu-id="6d841-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6d841-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d841-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d841-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d841-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6d841-127">INPUTS</span></span>

### <span data-ttu-id="6d841-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="6d841-128">None</span></span>
<span data-ttu-id="6d841-129">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="6d841-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6d841-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d841-130">OUTPUTS</span></span>

## <span data-ttu-id="6d841-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="6d841-131">NOTES</span></span>

## <span data-ttu-id="6d841-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6d841-132">RELATED LINKS</span></span>

[<span data-ttu-id="6d841-133">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="6d841-133">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)

[<span data-ttu-id="6d841-134">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="6d841-134">Set-AzureRmVMExtension</span></span>](./Set-AzureRmVMExtension.md)


