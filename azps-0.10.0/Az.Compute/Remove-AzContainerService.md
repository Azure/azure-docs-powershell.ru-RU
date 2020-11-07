---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 8180092D-5B1D-43A0-B830-D009B30E2DDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzContainerService.md
ms.openlocfilehash: 4a83b1c23b3c0cb9cdd86fde6f8aac4bb13f91ba
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911443"
---
# <span data-ttu-id="7139b-101">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="7139b-101">Remove-AzContainerService</span></span>

## <span data-ttu-id="7139b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7139b-102">SYNOPSIS</span></span>
<span data-ttu-id="7139b-103">Удаляет службу контейнера.</span><span class="sxs-lookup"><span data-stu-id="7139b-103">Removes a container service.</span></span>

## <span data-ttu-id="7139b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7139b-104">SYNTAX</span></span>

```
Remove-AzContainerService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7139b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7139b-105">DESCRIPTION</span></span>
<span data-ttu-id="7139b-106">Командлет **Remove-AzContainerService** Удаляет службу контейнеров из учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="7139b-106">The **Remove-AzContainerService** cmdlet removes a container service from your Azure account.</span></span>

## <span data-ttu-id="7139b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7139b-107">EXAMPLES</span></span>

### <span data-ttu-id="7139b-108">Пример 1: Удаление службы контейнеров</span><span class="sxs-lookup"><span data-stu-id="7139b-108">Example 1: Remove a container service</span></span>
```
PS C:\> Remove-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="7139b-109">Эта команда удаляет службу контейнеров с именем CSResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="7139b-109">This command removes the container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="7139b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7139b-110">PARAMETERS</span></span>

### <span data-ttu-id="7139b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7139b-111">-AsJob</span></span>
<span data-ttu-id="7139b-112">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="7139b-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="7139b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7139b-113">-DefaultProfile</span></span>
<span data-ttu-id="7139b-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7139b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7139b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="7139b-115">-Force</span></span>
<span data-ttu-id="7139b-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="7139b-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7139b-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7139b-117">-Name</span></span>
<span data-ttu-id="7139b-118">Указывает имя службы контейнеров, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="7139b-118">Specifies the name of the container service that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7139b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7139b-119">-ResourceGroupName</span></span>
<span data-ttu-id="7139b-120">Указывает группу ресурсов службы контейнеров, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="7139b-120">Specifies the resource group of the container service that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7139b-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7139b-121">-Confirm</span></span>
<span data-ttu-id="7139b-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7139b-122">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="7139b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7139b-123">-WhatIf</span></span>
<span data-ttu-id="7139b-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7139b-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7139b-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7139b-125">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="7139b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7139b-126">CommonParameters</span></span>
<span data-ttu-id="7139b-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7139b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7139b-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7139b-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7139b-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7139b-129">INPUTS</span></span>

### <span data-ttu-id="7139b-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="7139b-130">None</span></span>
<span data-ttu-id="7139b-131">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="7139b-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7139b-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7139b-132">OUTPUTS</span></span>

### <span data-ttu-id="7139b-133">System. void</span><span class="sxs-lookup"><span data-stu-id="7139b-133">System.Void</span></span>

## <span data-ttu-id="7139b-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="7139b-134">NOTES</span></span>

## <span data-ttu-id="7139b-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7139b-135">RELATED LINKS</span></span>

[<span data-ttu-id="7139b-136">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="7139b-136">Get-AzContainerService</span></span>](./Get-AzContainerService.md)

[<span data-ttu-id="7139b-137">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="7139b-137">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="7139b-138">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="7139b-138">Update-AzContainerService</span></span>](./Update-AzContainerService.md)


