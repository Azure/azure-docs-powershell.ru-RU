---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 22C490C2-0135-4375-897E-7224DBBE13A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMAccessExtension.md
ms.openlocfilehash: 0360bcdb766de681ab6f54682007076e18266051
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732119"
---
# <span data-ttu-id="8d9df-101">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="8d9df-101">Remove-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="8d9df-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8d9df-102">SYNOPSIS</span></span>
<span data-ttu-id="8d9df-103">Удаляет расширение VMAccess из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="8d9df-103">Removes the VMAccess extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d9df-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8d9df-104">SYNTAX</span></span>

```
Remove-AzureRmVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d9df-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d9df-105">DESCRIPTION</span></span>
<span data-ttu-id="8d9df-106">Командлет **Remove-AzureRmVMAccessExtension** удаляет расширение виртуальной машины доступа к виртуальной машине (VMAccess) с виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="8d9df-106">The **Remove-AzureRmVMAccessExtension** cmdlet removes the Virtual Machine Access (VMAccess) Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="8d9df-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8d9df-107">EXAMPLES</span></span>

## <span data-ttu-id="8d9df-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8d9df-108">PARAMETERS</span></span>

### <span data-ttu-id="8d9df-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d9df-109">-DefaultProfile</span></span>
<span data-ttu-id="8d9df-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8d9df-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d9df-111">-Force</span><span class="sxs-lookup"><span data-stu-id="8d9df-111">-Force</span></span>
<span data-ttu-id="8d9df-112">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="8d9df-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8d9df-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8d9df-113">-Name</span></span>
<span data-ttu-id="8d9df-114">Указывает имя расширения, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="8d9df-114">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8d9df-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d9df-115">-ResourceGroupName</span></span>
<span data-ttu-id="8d9df-116">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="8d9df-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="8d9df-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="8d9df-117">-VMName</span></span>
<span data-ttu-id="8d9df-118">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="8d9df-118">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="8d9df-119">Этот командлет удаляет VMAccess для виртуальной машины, указывающей этот параметр.</span><span class="sxs-lookup"><span data-stu-id="8d9df-119">This cmdlet removes VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="8d9df-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8d9df-120">-Confirm</span></span>
<span data-ttu-id="8d9df-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8d9df-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d9df-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d9df-122">-WhatIf</span></span>
<span data-ttu-id="8d9df-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8d9df-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d9df-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8d9df-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d9df-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d9df-125">CommonParameters</span></span>
<span data-ttu-id="8d9df-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8d9df-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d9df-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d9df-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d9df-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8d9df-128">INPUTS</span></span>

### <span data-ttu-id="8d9df-129">System. String</span><span class="sxs-lookup"><span data-stu-id="8d9df-129">System.String</span></span>

## <span data-ttu-id="8d9df-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d9df-130">OUTPUTS</span></span>

### <span data-ttu-id="8d9df-131">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="8d9df-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="8d9df-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="8d9df-132">NOTES</span></span>

## <span data-ttu-id="8d9df-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8d9df-133">RELATED LINKS</span></span>

[<span data-ttu-id="8d9df-134">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="8d9df-134">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="8d9df-135">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="8d9df-135">Set-AzureRmVMAccessExtension</span></span>](./Set-AzureRmVMAccessExtension.md)

[<span data-ttu-id="8d9df-136">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="8d9df-136">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)
