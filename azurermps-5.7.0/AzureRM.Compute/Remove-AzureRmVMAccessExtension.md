---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 22C490C2-0135-4375-897E-7224DBBE13A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMAccessExtension.md
ms.openlocfilehash: 16095113dcc0604bfb7b739b1227db337a0cf6f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563668"
---
# <span data-ttu-id="7cf51-101">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="7cf51-101">Remove-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="7cf51-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7cf51-102">SYNOPSIS</span></span>
<span data-ttu-id="7cf51-103">Удаляет расширение VMAccess из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="7cf51-103">Removes the VMAccess extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7cf51-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7cf51-104">SYNTAX</span></span>

```
Remove-AzureRmVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7cf51-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7cf51-105">DESCRIPTION</span></span>
<span data-ttu-id="7cf51-106">Командлет **Remove-AzureRmVMAccessExtension** удаляет расширение виртуальной машины доступа к виртуальной машине (VMAccess) с виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="7cf51-106">The **Remove-AzureRmVMAccessExtension** cmdlet removes the Virtual Machine Access (VMAccess) Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="7cf51-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7cf51-107">EXAMPLES</span></span>

## <span data-ttu-id="7cf51-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7cf51-108">PARAMETERS</span></span>

### <span data-ttu-id="7cf51-109">-Force</span><span class="sxs-lookup"><span data-stu-id="7cf51-109">-Force</span></span>
<span data-ttu-id="7cf51-110">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="7cf51-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7cf51-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7cf51-111">-Name</span></span>
<span data-ttu-id="7cf51-112">Указывает имя расширения, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="7cf51-112">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7cf51-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cf51-113">-ResourceGroupName</span></span>
<span data-ttu-id="7cf51-114">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="7cf51-114">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="7cf51-115">-VMName</span><span class="sxs-lookup"><span data-stu-id="7cf51-115">-VMName</span></span>
<span data-ttu-id="7cf51-116">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="7cf51-116">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="7cf51-117">Этот командлет удаляет VMAccess для виртуальной машины, указывающей этот параметр.</span><span class="sxs-lookup"><span data-stu-id="7cf51-117">This cmdlet removes VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="7cf51-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7cf51-118">-Confirm</span></span>
<span data-ttu-id="7cf51-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7cf51-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cf51-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cf51-120">-WhatIf</span></span>
<span data-ttu-id="7cf51-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7cf51-121">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="7cf51-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7cf51-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cf51-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cf51-123">CommonParameters</span></span>
<span data-ttu-id="7cf51-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7cf51-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cf51-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cf51-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cf51-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7cf51-126">INPUTS</span></span>

### <span data-ttu-id="7cf51-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="7cf51-127">None</span></span>
<span data-ttu-id="7cf51-128">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="7cf51-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7cf51-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7cf51-129">OUTPUTS</span></span>

## <span data-ttu-id="7cf51-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="7cf51-130">NOTES</span></span>

## <span data-ttu-id="7cf51-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7cf51-131">RELATED LINKS</span></span>

[<span data-ttu-id="7cf51-132">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="7cf51-132">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="7cf51-133">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="7cf51-133">Set-AzureRmVMAccessExtension</span></span>](./Set-AzureRmVMAccessExtension.md)

[<span data-ttu-id="7cf51-134">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="7cf51-134">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)
