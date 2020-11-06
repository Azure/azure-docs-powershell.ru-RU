---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7C3CF963-6F1A-444C-B90C-C1D24F89204D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Stop-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Stop-AzureRmVM.md
ms.openlocfilehash: f0d6ab84e457894b3c1ff7309efc6914350a03e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566744"
---
# <span data-ttu-id="ff522-101">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ff522-101">Stop-AzureRmVM</span></span>

## <span data-ttu-id="ff522-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ff522-102">SYNOPSIS</span></span>
<span data-ttu-id="ff522-103">Остановка виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="ff522-103">Stops an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff522-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ff522-104">SYNTAX</span></span>

### <span data-ttu-id="ff522-105">ResourceGroupNameParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ff522-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Stop-AzureRmVM [-Name] <String> [-Force] [-StayProvisioned] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff522-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="ff522-106">IdParameterSetName</span></span>
```
Stop-AzureRmVM [-Name] <String> [-Force] [-StayProvisioned] [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff522-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff522-107">DESCRIPTION</span></span>
<span data-ttu-id="ff522-108">Командлет **Stop-AzureRmVM** останавливает виртуальную машину Azure.</span><span class="sxs-lookup"><span data-stu-id="ff522-108">The **Stop-AzureRmVM** cmdlet stops an Azure virtual machine.</span></span>

## <span data-ttu-id="ff522-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ff522-109">EXAMPLES</span></span>

### <span data-ttu-id="ff522-110">Пример 1: остановка виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="ff522-110">Example 1: Stop a virtual machine</span></span>
```
PS C:\> Stop-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="ff522-111">Эта команда останавливает виртуальную машину с именем VirtualMachine07 в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="ff522-111">This command stops the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="ff522-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ff522-112">PARAMETERS</span></span>

### <span data-ttu-id="ff522-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff522-113">-DefaultProfile</span></span>
<span data-ttu-id="ff522-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ff522-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff522-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ff522-115">-Force</span></span>
<span data-ttu-id="ff522-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="ff522-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ff522-117">-ID</span><span class="sxs-lookup"><span data-stu-id="ff522-117">-Id</span></span>
<span data-ttu-id="ff522-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ff522-118">The resource group name.</span></span>

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

### <span data-ttu-id="ff522-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ff522-119">-Name</span></span>
<span data-ttu-id="ff522-120">Имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ff522-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="ff522-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff522-121">-ResourceGroupName</span></span>
<span data-ttu-id="ff522-122">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ff522-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="ff522-123">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="ff522-123">-StayProvisioned</span></span>
<span data-ttu-id="ff522-124">Командлет останавливает все виртуальные машины в VMSS, но не освобождает их.</span><span class="sxs-lookup"><span data-stu-id="ff522-124">The cmdlet stops all the virtual machines within the VMSS but does not deallocate them.</span></span> <span data-ttu-id="ff522-125">Учетная запись оплачивается для остановленных виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="ff522-125">The account is charged for the stopped virtual machines.</span></span>

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

### <span data-ttu-id="ff522-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ff522-126">-Confirm</span></span>
<span data-ttu-id="ff522-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ff522-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff522-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff522-128">-WhatIf</span></span>
<span data-ttu-id="ff522-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ff522-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ff522-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ff522-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff522-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff522-131">CommonParameters</span></span>
<span data-ttu-id="ff522-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ff522-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff522-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff522-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff522-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ff522-134">INPUTS</span></span>

## <span data-ttu-id="ff522-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff522-135">OUTPUTS</span></span>

## <span data-ttu-id="ff522-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="ff522-136">NOTES</span></span>

## <span data-ttu-id="ff522-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ff522-137">RELATED LINKS</span></span>

[<span data-ttu-id="ff522-138">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ff522-138">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="ff522-139">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ff522-139">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="ff522-140">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ff522-140">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="ff522-141">Restarting-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ff522-141">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="ff522-142">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ff522-142">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="ff522-143">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ff522-143">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


