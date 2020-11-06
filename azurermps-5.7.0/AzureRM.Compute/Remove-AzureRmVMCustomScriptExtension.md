---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: A65E82D5-706B-4470-A51E-936E381DA78F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMCustomScriptExtension.md
ms.openlocfilehash: 1e2dc6fe56cfaf182fb0614121ad9511edcfc2fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563660"
---
# <span data-ttu-id="b27e1-101">Remove-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="b27e1-101">Remove-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="b27e1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b27e1-102">SYNOPSIS</span></span>
<span data-ttu-id="b27e1-103">Удаляет настраиваемое расширение сценария из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b27e1-103">Removes a custom script extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b27e1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b27e1-104">SYNTAX</span></span>

```
Remove-AzureRmVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b27e1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b27e1-105">DESCRIPTION</span></span>
<span data-ttu-id="b27e1-106">Командлет **Remove-AzureRmVMCustomScriptExtension** удаляет расширение виртуальной машины специального сценария из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b27e1-106">The **Remove-AzureRmVMCustomScriptExtension** cmdlet removes a custom script Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="b27e1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b27e1-107">EXAMPLES</span></span>

## <span data-ttu-id="b27e1-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b27e1-108">PARAMETERS</span></span>

### <span data-ttu-id="b27e1-109">-Force</span><span class="sxs-lookup"><span data-stu-id="b27e1-109">-Force</span></span>
<span data-ttu-id="b27e1-110">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="b27e1-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b27e1-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b27e1-111">-Name</span></span>
<span data-ttu-id="b27e1-112">Указывает имя настраиваемого расширения скрипта, которое удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="b27e1-112">Specifies the name of the custom script extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b27e1-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b27e1-113">-ResourceGroupName</span></span>
<span data-ttu-id="b27e1-114">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b27e1-114">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="b27e1-115">-VMName</span><span class="sxs-lookup"><span data-stu-id="b27e1-115">-VMName</span></span>
<span data-ttu-id="b27e1-116">Указывает имя виртуальной машины, с помощью которой этот командлет удаляет настраиваемое расширение сценария.</span><span class="sxs-lookup"><span data-stu-id="b27e1-116">Specifies the name of a virtual machine from which this cmdlet removes the custom script extension.</span></span>

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

### <span data-ttu-id="b27e1-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b27e1-117">-Confirm</span></span>
<span data-ttu-id="b27e1-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b27e1-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b27e1-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b27e1-119">-WhatIf</span></span>
<span data-ttu-id="b27e1-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b27e1-120">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="b27e1-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b27e1-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b27e1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b27e1-122">CommonParameters</span></span>
<span data-ttu-id="b27e1-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b27e1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b27e1-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b27e1-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b27e1-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b27e1-125">INPUTS</span></span>

### <span data-ttu-id="b27e1-126">Ничего</span><span class="sxs-lookup"><span data-stu-id="b27e1-126">None</span></span>
<span data-ttu-id="b27e1-127">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="b27e1-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b27e1-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b27e1-128">OUTPUTS</span></span>

## <span data-ttu-id="b27e1-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="b27e1-129">NOTES</span></span>

## <span data-ttu-id="b27e1-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b27e1-130">RELATED LINKS</span></span>

[<span data-ttu-id="b27e1-131">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="b27e1-131">Get-AzureRmVMCustomScriptExtension</span></span>](./Get-AzureRmVMCustomScriptExtension.md)

[<span data-ttu-id="b27e1-132">Set-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="b27e1-132">Set-AzureRmVMCustomScriptExtension</span></span>](./Set-AzureRmVMCustomScriptExtension.md)
