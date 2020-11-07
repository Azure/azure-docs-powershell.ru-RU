---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 6C40A7BA-6BE2-464A-84E4-9021935A5BF6
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMExtension.md
ms.openlocfilehash: e1b400f2fe3ff973c586fbde9f4003732ad8c6cb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911409"
---
# <span data-ttu-id="1fa9c-101">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="1fa9c-101">Remove-AzVMExtension</span></span>

## <span data-ttu-id="1fa9c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1fa9c-102">SYNOPSIS</span></span>
<span data-ttu-id="1fa9c-103">Удаляет расширение из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="1fa9c-103">Removes an extension from a virtual machine.</span></span>

## <span data-ttu-id="1fa9c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1fa9c-104">SYNTAX</span></span>

```
Remove-AzVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fa9c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1fa9c-105">DESCRIPTION</span></span>
<span data-ttu-id="1fa9c-106">Командлет **Remove-AzVMExtension** удаляет расширение из расширений виртуальных машин виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="1fa9c-106">The **Remove-AzVMExtension** cmdlet removes an extension from the Virtual Machine Extensions of a virtual machine.</span></span>

## <span data-ttu-id="1fa9c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1fa9c-107">EXAMPLES</span></span>

### <span data-ttu-id="1fa9c-108">Пример 1: удаление расширения из виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="1fa9c-108">Example 1: Remove an extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMExtension -ResourceGroupName "ResourceGroup11" -Name "ContosoTest" -VMName "VirtualMachine22"
```

<span data-ttu-id="1fa9c-109">Эта команда удаляет расширение ContosoTest с виртуальной машины с именем VirtualMachine22 в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="1fa9c-109">This command removes the extension named ContosoTest from the virtual machine named VirtualMachine22 in ResourceGroup11.</span></span>

## <span data-ttu-id="1fa9c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1fa9c-110">PARAMETERS</span></span>

### <span data-ttu-id="1fa9c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fa9c-111">-DefaultProfile</span></span>
<span data-ttu-id="1fa9c-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1fa9c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1fa9c-113">-Force</span><span class="sxs-lookup"><span data-stu-id="1fa9c-113">-Force</span></span>
<span data-ttu-id="1fa9c-114">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="1fa9c-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1fa9c-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1fa9c-115">-Name</span></span>
<span data-ttu-id="1fa9c-116">Указывает имя расширения, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="1fa9c-116">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1fa9c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fa9c-117">-ResourceGroupName</span></span>
<span data-ttu-id="1fa9c-118">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="1fa9c-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="1fa9c-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="1fa9c-119">-VMName</span></span>
<span data-ttu-id="1fa9c-120">Указывает имя виртуальной машины, с помощью которой этот командлет удаляет расширение.</span><span class="sxs-lookup"><span data-stu-id="1fa9c-120">Specifies the name of a virtual machine from which this cmdlet removes the extension.</span></span>

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

### <span data-ttu-id="1fa9c-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1fa9c-121">-Confirm</span></span>
<span data-ttu-id="1fa9c-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1fa9c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fa9c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fa9c-123">-WhatIf</span></span>
<span data-ttu-id="1fa9c-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1fa9c-124">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="1fa9c-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1fa9c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fa9c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fa9c-126">CommonParameters</span></span>
<span data-ttu-id="1fa9c-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1fa9c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fa9c-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fa9c-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fa9c-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1fa9c-129">INPUTS</span></span>

### <span data-ttu-id="1fa9c-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="1fa9c-130">None</span></span>
<span data-ttu-id="1fa9c-131">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="1fa9c-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1fa9c-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1fa9c-132">OUTPUTS</span></span>

### <span data-ttu-id="1fa9c-133">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="1fa9c-133">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="1fa9c-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="1fa9c-134">NOTES</span></span>

## <span data-ttu-id="1fa9c-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1fa9c-135">RELATED LINKS</span></span>

[<span data-ttu-id="1fa9c-136">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="1fa9c-136">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="1fa9c-137">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="1fa9c-137">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)


