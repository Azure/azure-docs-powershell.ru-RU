---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: A65E82D5-706B-4470-A51E-936E381DA78F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmcustomscriptextension
schema: 2.0.0
ms.openlocfilehash: 70715c4bb4c3e5f805f297c8b68def0f5b3a0d6f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914514"
---
# <span data-ttu-id="9c91a-101">Remove-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="9c91a-101">Remove-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="9c91a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9c91a-102">SYNOPSIS</span></span>
<span data-ttu-id="9c91a-103">Удаляет настраиваемое расширение сценария из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9c91a-103">Removes a custom script extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c91a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9c91a-104">SYNTAX</span></span>

```
Remove-AzureRmVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c91a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c91a-105">DESCRIPTION</span></span>
<span data-ttu-id="9c91a-106">Командлет **Remove-AzureRmVMCustomScriptExtension** удаляет расширение виртуальной машины специального сценария из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9c91a-106">The **Remove-AzureRmVMCustomScriptExtension** cmdlet removes a custom script Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="9c91a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9c91a-107">EXAMPLES</span></span>

## <span data-ttu-id="9c91a-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9c91a-108">PARAMETERS</span></span>

### <span data-ttu-id="9c91a-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c91a-109">-DefaultProfile</span></span>
<span data-ttu-id="9c91a-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9c91a-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c91a-111">-Force</span><span class="sxs-lookup"><span data-stu-id="9c91a-111">-Force</span></span>
<span data-ttu-id="9c91a-112">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="9c91a-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9c91a-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9c91a-113">-Name</span></span>
<span data-ttu-id="9c91a-114">Указывает имя настраиваемого расширения скрипта, которое удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="9c91a-114">Specifies the name of the custom script extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9c91a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c91a-115">-ResourceGroupName</span></span>
<span data-ttu-id="9c91a-116">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9c91a-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="9c91a-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="9c91a-117">-VMName</span></span>
<span data-ttu-id="9c91a-118">Указывает имя виртуальной машины, с помощью которой этот командлет удаляет настраиваемое расширение сценария.</span><span class="sxs-lookup"><span data-stu-id="9c91a-118">Specifies the name of a virtual machine from which this cmdlet removes the custom script extension.</span></span>

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

### <span data-ttu-id="9c91a-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9c91a-119">-Confirm</span></span>
<span data-ttu-id="9c91a-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9c91a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c91a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c91a-121">-WhatIf</span></span>
<span data-ttu-id="9c91a-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9c91a-122">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="9c91a-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9c91a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c91a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c91a-124">CommonParameters</span></span>
<span data-ttu-id="9c91a-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9c91a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c91a-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c91a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c91a-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9c91a-127">INPUTS</span></span>

### <span data-ttu-id="9c91a-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="9c91a-128">None</span></span>
<span data-ttu-id="9c91a-129">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="9c91a-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9c91a-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c91a-130">OUTPUTS</span></span>

### <span data-ttu-id="9c91a-131">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9c91a-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="9c91a-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="9c91a-132">NOTES</span></span>

## <span data-ttu-id="9c91a-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9c91a-133">RELATED LINKS</span></span>

[<span data-ttu-id="9c91a-134">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="9c91a-134">Get-AzureRmVMCustomScriptExtension</span></span>](./Get-AzureRmVMCustomScriptExtension.md)

[<span data-ttu-id="9c91a-135">Set-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="9c91a-135">Set-AzureRmVMCustomScriptExtension</span></span>](./Set-AzureRmVMCustomScriptExtension.md)
