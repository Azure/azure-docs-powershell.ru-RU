---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: A16C2084-30A4-4AB8-AE22-28CC6E74FD48
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVM.md
ms.openlocfilehash: 3cc48d103867008b247ce480de43d1ccadc68d18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567142"
---
# <span data-ttu-id="f0d18-101">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f0d18-101">Remove-AzureRmVM</span></span>

## <span data-ttu-id="f0d18-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f0d18-102">SYNOPSIS</span></span>
<span data-ttu-id="f0d18-103">Удаление виртуальной машины из Azure.</span><span class="sxs-lookup"><span data-stu-id="f0d18-103">Removes a virtual machine from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f0d18-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f0d18-104">SYNTAX</span></span>

### <span data-ttu-id="f0d18-105">ResourceGroupNameParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f0d18-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Remove-AzureRmVM [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0d18-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="f0d18-106">IdParameterSetName</span></span>
```
Remove-AzureRmVM [-Name] <String> [-Force] [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0d18-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0d18-107">DESCRIPTION</span></span>
<span data-ttu-id="f0d18-108">Командлет **Remove-AzureRmVM** удаляет виртуальную машину из Azure.</span><span class="sxs-lookup"><span data-stu-id="f0d18-108">The **Remove-AzureRmVM** cmdlet removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="f0d18-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f0d18-109">EXAMPLES</span></span>

### <span data-ttu-id="f0d18-110">Пример 1: Удаление виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="f0d18-110">Example 1: Remove a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="f0d18-111">Эта команда удаляет виртуальную машину с именем VirtualMachine07 в группе ресурсов ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="f0d18-111">This command removes the virtual machine named VirtualMachine07 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="f0d18-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f0d18-112">PARAMETERS</span></span>

### <span data-ttu-id="f0d18-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0d18-113">-DefaultProfile</span></span>
<span data-ttu-id="f0d18-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f0d18-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0d18-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f0d18-115">-Force</span></span>
<span data-ttu-id="f0d18-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="f0d18-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0d18-117">-ID</span><span class="sxs-lookup"><span data-stu-id="f0d18-117">-Id</span></span>
<span data-ttu-id="f0d18-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f0d18-118">The resource group name.</span></span>

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

### <span data-ttu-id="f0d18-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f0d18-119">-Name</span></span>
<span data-ttu-id="f0d18-120">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="f0d18-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0d18-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0d18-121">-ResourceGroupName</span></span>
<span data-ttu-id="f0d18-122">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f0d18-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f0d18-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f0d18-123">-Confirm</span></span>
<span data-ttu-id="f0d18-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f0d18-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0d18-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0d18-125">-WhatIf</span></span>
<span data-ttu-id="f0d18-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f0d18-126">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="f0d18-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f0d18-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0d18-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0d18-128">CommonParameters</span></span>
<span data-ttu-id="f0d18-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f0d18-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0d18-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0d18-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0d18-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f0d18-131">INPUTS</span></span>

## <span data-ttu-id="f0d18-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0d18-132">OUTPUTS</span></span>

## <span data-ttu-id="f0d18-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="f0d18-133">NOTES</span></span>

## <span data-ttu-id="f0d18-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f0d18-134">RELATED LINKS</span></span>

[<span data-ttu-id="f0d18-135">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f0d18-135">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="f0d18-136">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f0d18-136">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="f0d18-137">Restarting-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f0d18-137">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="f0d18-138">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f0d18-138">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="f0d18-139">Остановить-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f0d18-139">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="f0d18-140">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f0d18-140">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


