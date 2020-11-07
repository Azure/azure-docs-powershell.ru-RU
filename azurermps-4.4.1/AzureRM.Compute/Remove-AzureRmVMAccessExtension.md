---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 22C490C2-0135-4375-897E-7224DBBE13A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMAccessExtension.md
ms.openlocfilehash: 97ddf35b453b324cf04309afd3a90be185d43224
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733392"
---
# <span data-ttu-id="fae94-101">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="fae94-101">Remove-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="fae94-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fae94-102">SYNOPSIS</span></span>
<span data-ttu-id="fae94-103">Удаляет расширение VMAccess из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="fae94-103">Removes the VMAccess extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fae94-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fae94-104">SYNTAX</span></span>

```
Remove-AzureRmVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fae94-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fae94-105">DESCRIPTION</span></span>
<span data-ttu-id="fae94-106">Командлет **Remove-AzureRmVMAccessExtension** удаляет расширение виртуальной машины доступа к виртуальной машине (VMAccess) с виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="fae94-106">The **Remove-AzureRmVMAccessExtension** cmdlet removes the Virtual Machine Access (VMAccess) Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="fae94-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fae94-107">EXAMPLES</span></span>

## <span data-ttu-id="fae94-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fae94-108">PARAMETERS</span></span>

### <span data-ttu-id="fae94-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fae94-109">-DefaultProfile</span></span>
<span data-ttu-id="fae94-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fae94-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fae94-111">-Force</span><span class="sxs-lookup"><span data-stu-id="fae94-111">-Force</span></span>
<span data-ttu-id="fae94-112">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="fae94-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fae94-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fae94-113">-Name</span></span>
<span data-ttu-id="fae94-114">Указывает имя расширения, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="fae94-114">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="fae94-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fae94-115">-ResourceGroupName</span></span>
<span data-ttu-id="fae94-116">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="fae94-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="fae94-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="fae94-117">-VMName</span></span>
<span data-ttu-id="fae94-118">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="fae94-118">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="fae94-119">Этот командлет удаляет VMAccess для виртуальной машины, указывающей этот параметр.</span><span class="sxs-lookup"><span data-stu-id="fae94-119">This cmdlet removes VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="fae94-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fae94-120">-Confirm</span></span>
<span data-ttu-id="fae94-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fae94-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fae94-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fae94-122">-WhatIf</span></span>
<span data-ttu-id="fae94-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fae94-123">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="fae94-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fae94-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fae94-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fae94-125">CommonParameters</span></span>
<span data-ttu-id="fae94-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fae94-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fae94-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fae94-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fae94-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fae94-128">INPUTS</span></span>

## <span data-ttu-id="fae94-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fae94-129">OUTPUTS</span></span>

## <span data-ttu-id="fae94-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="fae94-130">NOTES</span></span>

## <span data-ttu-id="fae94-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fae94-131">RELATED LINKS</span></span>

[<span data-ttu-id="fae94-132">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="fae94-132">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="fae94-133">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="fae94-133">Set-AzureRmVMAccessExtension</span></span>](./Set-AzureRmVMAccessExtension.md)

[<span data-ttu-id="fae94-134">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="fae94-134">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)
