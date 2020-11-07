---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: A65E82D5-706B-4470-A51E-936E381DA78F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMCustomScriptExtension.md
ms.openlocfilehash: ee0762dfa78a5bd863ede7b56cb746c2c8cab3be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734681"
---
# <span data-ttu-id="8b6b3-101">Remove-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="8b6b3-101">Remove-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="8b6b3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8b6b3-102">SYNOPSIS</span></span>
<span data-ttu-id="8b6b3-103">Удаляет настраиваемое расширение сценария из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="8b6b3-103">Removes a custom script extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b6b3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8b6b3-104">SYNTAX</span></span>

```
Remove-AzureRmVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b6b3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8b6b3-105">DESCRIPTION</span></span>
<span data-ttu-id="8b6b3-106">Командлет **Remove-AzureRmVMCustomScriptExtension** удаляет расширение виртуальной машины специального сценария из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="8b6b3-106">The **Remove-AzureRmVMCustomScriptExtension** cmdlet removes a custom script Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="8b6b3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8b6b3-107">EXAMPLES</span></span>

## <span data-ttu-id="8b6b3-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8b6b3-108">PARAMETERS</span></span>

### <span data-ttu-id="8b6b3-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b6b3-109">-DefaultProfile</span></span>
<span data-ttu-id="8b6b3-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8b6b3-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b6b3-111">-Force</span><span class="sxs-lookup"><span data-stu-id="8b6b3-111">-Force</span></span>
<span data-ttu-id="8b6b3-112">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="8b6b3-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8b6b3-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8b6b3-113">-Name</span></span>
<span data-ttu-id="8b6b3-114">Указывает имя настраиваемого расширения скрипта, которое удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="8b6b3-114">Specifies the name of the custom script extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8b6b3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b6b3-115">-ResourceGroupName</span></span>
<span data-ttu-id="8b6b3-116">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="8b6b3-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="8b6b3-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="8b6b3-117">-VMName</span></span>
<span data-ttu-id="8b6b3-118">Указывает имя виртуальной машины, с помощью которой этот командлет удаляет настраиваемое расширение сценария.</span><span class="sxs-lookup"><span data-stu-id="8b6b3-118">Specifies the name of a virtual machine from which this cmdlet removes the custom script extension.</span></span>

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

### <span data-ttu-id="8b6b3-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8b6b3-119">-Confirm</span></span>
<span data-ttu-id="8b6b3-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8b6b3-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b6b3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b6b3-121">-WhatIf</span></span>
<span data-ttu-id="8b6b3-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8b6b3-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b6b3-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8b6b3-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b6b3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b6b3-124">CommonParameters</span></span>
<span data-ttu-id="8b6b3-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8b6b3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b6b3-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b6b3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b6b3-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8b6b3-127">INPUTS</span></span>

### <span data-ttu-id="8b6b3-128">System. String</span><span class="sxs-lookup"><span data-stu-id="8b6b3-128">System.String</span></span>

## <span data-ttu-id="8b6b3-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8b6b3-129">OUTPUTS</span></span>

### <span data-ttu-id="8b6b3-130">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="8b6b3-130">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="8b6b3-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="8b6b3-131">NOTES</span></span>

## <span data-ttu-id="8b6b3-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8b6b3-132">RELATED LINKS</span></span>

[<span data-ttu-id="8b6b3-133">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="8b6b3-133">Get-AzureRmVMCustomScriptExtension</span></span>](./Get-AzureRmVMCustomScriptExtension.md)

[<span data-ttu-id="8b6b3-134">Set-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="8b6b3-134">Set-AzureRmVMCustomScriptExtension</span></span>](./Set-AzureRmVMCustomScriptExtension.md)
