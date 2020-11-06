---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7320B832-50FD-48AE-9089-445318F3B08A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmAvailabilitySet.md
ms.openlocfilehash: 7efbfd633b87603d22b5009be71e07895442d893
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561032"
---
# <span data-ttu-id="f38cc-101">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f38cc-101">Remove-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="f38cc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f38cc-102">SYNOPSIS</span></span>
<span data-ttu-id="f38cc-103">Удаляет группу доступности из Azure.</span><span class="sxs-lookup"><span data-stu-id="f38cc-103">Removes an availability set from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f38cc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f38cc-104">SYNTAX</span></span>

```
Remove-AzureRmAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f38cc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f38cc-105">DESCRIPTION</span></span>
<span data-ttu-id="f38cc-106">Командлет **Remove-AzureRmAvailabilitySet** удаляет группу доступности из Azure.</span><span class="sxs-lookup"><span data-stu-id="f38cc-106">The **Remove-AzureRmAvailabilitySet** cmdlet removes an availability set from Azure.</span></span>

## <span data-ttu-id="f38cc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f38cc-107">EXAMPLES</span></span>

### <span data-ttu-id="f38cc-108">Пример 1: Удаление группы доступности</span><span class="sxs-lookup"><span data-stu-id="f38cc-108">Example 1: Remove an availability set</span></span>
```
PS C:\> Remove-AzureRmAvailabilitySet -Name "AvailabilitySet03" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="f38cc-109">Эта команда удаляет группу доступности с именем AvailablitySet03 в группе ресурсов с именем ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="f38cc-109">This command removes an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="f38cc-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f38cc-110">PARAMETERS</span></span>

### <span data-ttu-id="f38cc-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f38cc-111">-AsJob</span></span>
<span data-ttu-id="f38cc-112">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="f38cc-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="f38cc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f38cc-113">-DefaultProfile</span></span>
<span data-ttu-id="f38cc-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f38cc-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f38cc-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f38cc-115">-Force</span></span>
<span data-ttu-id="f38cc-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="f38cc-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f38cc-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f38cc-117">-Name</span></span>
<span data-ttu-id="f38cc-118">Имя группы доступности.</span><span class="sxs-lookup"><span data-stu-id="f38cc-118">The availability set name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f38cc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f38cc-119">-ResourceGroupName</span></span>
<span data-ttu-id="f38cc-120">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f38cc-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f38cc-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f38cc-121">-Confirm</span></span>
<span data-ttu-id="f38cc-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f38cc-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f38cc-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f38cc-123">-WhatIf</span></span>
<span data-ttu-id="f38cc-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f38cc-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f38cc-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f38cc-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f38cc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f38cc-126">CommonParameters</span></span>
<span data-ttu-id="f38cc-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f38cc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f38cc-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f38cc-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f38cc-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f38cc-129">INPUTS</span></span>

### <span data-ttu-id="f38cc-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f38cc-130">System.String</span></span>

## <span data-ttu-id="f38cc-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f38cc-131">OUTPUTS</span></span>

### <span data-ttu-id="f38cc-132">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f38cc-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="f38cc-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="f38cc-133">NOTES</span></span>

## <span data-ttu-id="f38cc-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f38cc-134">RELATED LINKS</span></span>

[<span data-ttu-id="f38cc-135">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f38cc-135">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="f38cc-136">New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="f38cc-136">New-AzureRmAvailabilitySet</span></span>](./New-AzureRmAvailabilitySet.md)


