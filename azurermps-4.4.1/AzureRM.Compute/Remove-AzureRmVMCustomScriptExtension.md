---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: A65E82D5-706B-4470-A51E-936E381DA78F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMCustomScriptExtension.md
ms.openlocfilehash: 2d1edd8e511042f677928f171d7e31859cc5390f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557900"
---
# <span data-ttu-id="a61c9-101">Remove-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="a61c9-101">Remove-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="a61c9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a61c9-102">SYNOPSIS</span></span>
<span data-ttu-id="a61c9-103">Удаляет настраиваемое расширение сценария из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a61c9-103">Removes a custom script extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a61c9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a61c9-104">SYNTAX</span></span>

```
Remove-AzureRmVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a61c9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a61c9-105">DESCRIPTION</span></span>
<span data-ttu-id="a61c9-106">Командлет **Remove-AzureRmVMCustomScriptExtension** удаляет расширение виртуальной машины специального сценария из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a61c9-106">The **Remove-AzureRmVMCustomScriptExtension** cmdlet removes a custom script Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="a61c9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a61c9-107">EXAMPLES</span></span>

## <span data-ttu-id="a61c9-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a61c9-108">PARAMETERS</span></span>

### <span data-ttu-id="a61c9-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a61c9-109">-DefaultProfile</span></span>
<span data-ttu-id="a61c9-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a61c9-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a61c9-111">-Force</span><span class="sxs-lookup"><span data-stu-id="a61c9-111">-Force</span></span>
<span data-ttu-id="a61c9-112">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="a61c9-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a61c9-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a61c9-113">-Name</span></span>
<span data-ttu-id="a61c9-114">Указывает имя настраиваемого расширения скрипта, которое удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="a61c9-114">Specifies the name of the custom script extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a61c9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a61c9-115">-ResourceGroupName</span></span>
<span data-ttu-id="a61c9-116">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a61c9-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="a61c9-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="a61c9-117">-VMName</span></span>
<span data-ttu-id="a61c9-118">Указывает имя виртуальной машины, с помощью которой этот командлет удаляет настраиваемое расширение сценария.</span><span class="sxs-lookup"><span data-stu-id="a61c9-118">Specifies the name of a virtual machine from which this cmdlet removes the custom script extension.</span></span>

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

### <span data-ttu-id="a61c9-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a61c9-119">-Confirm</span></span>
<span data-ttu-id="a61c9-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a61c9-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a61c9-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a61c9-121">-WhatIf</span></span>
<span data-ttu-id="a61c9-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a61c9-122">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="a61c9-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a61c9-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a61c9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a61c9-124">CommonParameters</span></span>
<span data-ttu-id="a61c9-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a61c9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a61c9-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a61c9-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a61c9-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a61c9-127">INPUTS</span></span>

## <span data-ttu-id="a61c9-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a61c9-128">OUTPUTS</span></span>

## <span data-ttu-id="a61c9-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="a61c9-129">NOTES</span></span>

## <span data-ttu-id="a61c9-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a61c9-130">RELATED LINKS</span></span>

[<span data-ttu-id="a61c9-131">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="a61c9-131">Get-AzureRmVMCustomScriptExtension</span></span>](./Get-AzureRmVMCustomScriptExtension.md)

[<span data-ttu-id="a61c9-132">Set-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="a61c9-132">Set-AzureRmVMCustomScriptExtension</span></span>](./Set-AzureRmVMCustomScriptExtension.md)
