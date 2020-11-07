---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 22C490C2-0135-4375-897E-7224DBBE13A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmaccessextension
schema: 2.0.0
ms.openlocfilehash: 8d2646c56a8ac659f5beeb6695dc2899fb2f2542
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914522"
---
# <span data-ttu-id="cc647-101">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="cc647-101">Remove-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="cc647-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cc647-102">SYNOPSIS</span></span>
<span data-ttu-id="cc647-103">Удаляет расширение VMAccess из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="cc647-103">Removes the VMAccess extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc647-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cc647-104">SYNTAX</span></span>

```
Remove-AzureRmVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc647-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cc647-105">DESCRIPTION</span></span>
<span data-ttu-id="cc647-106">Командлет **Remove-AzureRmVMAccessExtension** удаляет расширение виртуальной машины доступа к виртуальной машине (VMAccess) с виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="cc647-106">The **Remove-AzureRmVMAccessExtension** cmdlet removes the Virtual Machine Access (VMAccess) Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="cc647-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cc647-107">EXAMPLES</span></span>

## <span data-ttu-id="cc647-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cc647-108">PARAMETERS</span></span>

### <span data-ttu-id="cc647-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc647-109">-DefaultProfile</span></span>
<span data-ttu-id="cc647-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cc647-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc647-111">-Force</span><span class="sxs-lookup"><span data-stu-id="cc647-111">-Force</span></span>
<span data-ttu-id="cc647-112">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="cc647-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cc647-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cc647-113">-Name</span></span>
<span data-ttu-id="cc647-114">Указывает имя расширения, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="cc647-114">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="cc647-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc647-115">-ResourceGroupName</span></span>
<span data-ttu-id="cc647-116">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="cc647-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="cc647-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="cc647-117">-VMName</span></span>
<span data-ttu-id="cc647-118">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="cc647-118">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="cc647-119">Этот командлет удаляет VMAccess для виртуальной машины, указывающей этот параметр.</span><span class="sxs-lookup"><span data-stu-id="cc647-119">This cmdlet removes VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="cc647-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cc647-120">-Confirm</span></span>
<span data-ttu-id="cc647-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cc647-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc647-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc647-122">-WhatIf</span></span>
<span data-ttu-id="cc647-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cc647-123">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="cc647-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cc647-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc647-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc647-125">CommonParameters</span></span>
<span data-ttu-id="cc647-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cc647-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc647-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc647-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc647-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cc647-128">INPUTS</span></span>

### <span data-ttu-id="cc647-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="cc647-129">None</span></span>
<span data-ttu-id="cc647-130">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="cc647-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cc647-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cc647-131">OUTPUTS</span></span>

### <span data-ttu-id="cc647-132">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="cc647-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="cc647-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="cc647-133">NOTES</span></span>

## <span data-ttu-id="cc647-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cc647-134">RELATED LINKS</span></span>

[<span data-ttu-id="cc647-135">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="cc647-135">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="cc647-136">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="cc647-136">Set-AzureRmVMAccessExtension</span></span>](./Set-AzureRmVMAccessExtension.md)

[<span data-ttu-id="cc647-137">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="cc647-137">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)
