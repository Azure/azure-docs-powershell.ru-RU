---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Start-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Start-AzureRmVM.md
ms.openlocfilehash: 3091cb877ff792527cf97e3d44b7c363f9dd94b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559939"
---
# <span data-ttu-id="3b8a8-101">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3b8a8-101">Start-AzureRmVM</span></span>

## <span data-ttu-id="3b8a8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3b8a8-102">SYNOPSIS</span></span>
<span data-ttu-id="3b8a8-103">Запуск виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="3b8a8-103">Starts an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b8a8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3b8a8-104">SYNTAX</span></span>

### <span data-ttu-id="3b8a8-105">ResourceGroupNameParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3b8a8-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzureRmVM [-Name] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b8a8-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="3b8a8-106">IdParameterSetName</span></span>
```
Start-AzureRmVM [-Name] <String> [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3b8a8-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3b8a8-107">DESCRIPTION</span></span>
<span data-ttu-id="3b8a8-108">Командлет **Start-AzureRmVM** запускает виртуальную машину Azure.</span><span class="sxs-lookup"><span data-stu-id="3b8a8-108">The **Start-AzureRmVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="3b8a8-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3b8a8-109">EXAMPLES</span></span>

### <span data-ttu-id="3b8a8-110">Пример 1: Запуск виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="3b8a8-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="3b8a8-111">Эта команда запускает виртуальную машину с именем VirtualMachine07 в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="3b8a8-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="3b8a8-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3b8a8-112">PARAMETERS</span></span>

### <span data-ttu-id="3b8a8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b8a8-113">-DefaultProfile</span></span>
<span data-ttu-id="3b8a8-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3b8a8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b8a8-115">-ID</span><span class="sxs-lookup"><span data-stu-id="3b8a8-115">-Id</span></span>
<span data-ttu-id="3b8a8-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3b8a8-116">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b8a8-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3b8a8-117">-Name</span></span>
<span data-ttu-id="3b8a8-118">Имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="3b8a8-118">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b8a8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b8a8-119">-ResourceGroupName</span></span>
<span data-ttu-id="3b8a8-120">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="3b8a8-120">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b8a8-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3b8a8-121">-Confirm</span></span>
<span data-ttu-id="3b8a8-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3b8a8-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b8a8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b8a8-123">-WhatIf</span></span>
<span data-ttu-id="3b8a8-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3b8a8-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3b8a8-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3b8a8-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b8a8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b8a8-126">CommonParameters</span></span>
<span data-ttu-id="3b8a8-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3b8a8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b8a8-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b8a8-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b8a8-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3b8a8-129">INPUTS</span></span>

## <span data-ttu-id="3b8a8-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3b8a8-130">OUTPUTS</span></span>

## <span data-ttu-id="3b8a8-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="3b8a8-131">NOTES</span></span>

## <span data-ttu-id="3b8a8-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3b8a8-132">RELATED LINKS</span></span>

[<span data-ttu-id="3b8a8-133">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3b8a8-133">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="3b8a8-134">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3b8a8-134">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="3b8a8-135">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3b8a8-135">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="3b8a8-136">Restarting-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3b8a8-136">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="3b8a8-137">Остановить-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3b8a8-137">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="3b8a8-138">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3b8a8-138">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


