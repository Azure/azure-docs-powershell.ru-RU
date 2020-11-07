---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: A65E82D5-706B-4470-A51E-936E381DA78F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMCustomScriptExtension.md
ms.openlocfilehash: 8bead12111148d193e0e5dfe880ed3b28c6dcd01
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911420"
---
# <span data-ttu-id="f2546-101">Remove-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="f2546-101">Remove-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="f2546-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f2546-102">SYNOPSIS</span></span>
<span data-ttu-id="f2546-103">Удаляет настраиваемое расширение сценария из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f2546-103">Removes a custom script extension from a virtual machine.</span></span>

## <span data-ttu-id="f2546-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f2546-104">SYNTAX</span></span>

```
Remove-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2546-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2546-105">DESCRIPTION</span></span>
<span data-ttu-id="f2546-106">Командлет **Remove-AzVMCustomScriptExtension** удаляет расширение виртуальной машины специального сценария из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f2546-106">The **Remove-AzVMCustomScriptExtension** cmdlet removes a custom script Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="f2546-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f2546-107">EXAMPLES</span></span>

## <span data-ttu-id="f2546-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f2546-108">PARAMETERS</span></span>

### <span data-ttu-id="f2546-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2546-109">-DefaultProfile</span></span>
<span data-ttu-id="f2546-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f2546-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2546-111">-Force</span><span class="sxs-lookup"><span data-stu-id="f2546-111">-Force</span></span>
<span data-ttu-id="f2546-112">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="f2546-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f2546-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f2546-113">-Name</span></span>
<span data-ttu-id="f2546-114">Указывает имя настраиваемого расширения скрипта, которое удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="f2546-114">Specifies the name of the custom script extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f2546-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2546-115">-ResourceGroupName</span></span>
<span data-ttu-id="f2546-116">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f2546-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="f2546-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="f2546-117">-VMName</span></span>
<span data-ttu-id="f2546-118">Указывает имя виртуальной машины, с помощью которой этот командлет удаляет настраиваемое расширение сценария.</span><span class="sxs-lookup"><span data-stu-id="f2546-118">Specifies the name of a virtual machine from which this cmdlet removes the custom script extension.</span></span>

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

### <span data-ttu-id="f2546-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f2546-119">-Confirm</span></span>
<span data-ttu-id="f2546-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f2546-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2546-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2546-121">-WhatIf</span></span>
<span data-ttu-id="f2546-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f2546-122">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="f2546-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f2546-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2546-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2546-124">CommonParameters</span></span>
<span data-ttu-id="f2546-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f2546-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2546-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2546-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2546-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f2546-127">INPUTS</span></span>

### <span data-ttu-id="f2546-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="f2546-128">None</span></span>
<span data-ttu-id="f2546-129">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="f2546-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f2546-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2546-130">OUTPUTS</span></span>

### <span data-ttu-id="f2546-131">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f2546-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="f2546-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="f2546-132">NOTES</span></span>

## <span data-ttu-id="f2546-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f2546-133">RELATED LINKS</span></span>

[<span data-ttu-id="f2546-134">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="f2546-134">Get-AzVMCustomScriptExtension</span></span>](./Get-AzVMCustomScriptExtension.md)

[<span data-ttu-id="f2546-135">Set-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="f2546-135">Set-AzVMCustomScriptExtension</span></span>](./Set-AzVMCustomScriptExtension.md)
