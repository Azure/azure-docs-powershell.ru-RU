---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationsecuritygroup
schema: 2.0.0
ms.openlocfilehash: 48121e165eea27b57ec36301a657a6778f4c14b7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913593"
---
# <span data-ttu-id="8bff7-101">Remove-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8bff7-101">Remove-AzureRmApplicationSecurityGroup</span></span>

## <span data-ttu-id="8bff7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8bff7-102">SYNOPSIS</span></span>
<span data-ttu-id="8bff7-103">Удаляет группу безопасности приложений.</span><span class="sxs-lookup"><span data-stu-id="8bff7-103">Removes an application security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8bff7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8bff7-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationSecurityGroup -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8bff7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8bff7-105">DESCRIPTION</span></span>
<span data-ttu-id="8bff7-106">Командлет **Remove-AzureRmApplicationSecurityGroup** удаляет группу безопасности приложений.</span><span class="sxs-lookup"><span data-stu-id="8bff7-106">The **Remove-AzureRmApplicationSecurityGroup** cmdlet removes an application security group.</span></span>

## <span data-ttu-id="8bff7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8bff7-107">EXAMPLES</span></span>

### <span data-ttu-id="8bff7-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8bff7-108">Example 1</span></span>
```
PS C:\>Remove-AzureRmApplicationSecurityGroup -Name "MyApplicationSecurityGrouo" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="8bff7-109">Эта команда удаляет группу безопасности приложений с именем MyApplicationSecurityGrouo в группе ресурсов с именем MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8bff7-109">This command deletes an application security group named MyApplicationSecurityGrouo in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="8bff7-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8bff7-110">PARAMETERS</span></span>

### <span data-ttu-id="8bff7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bff7-111">-DefaultProfile</span></span>
<span data-ttu-id="8bff7-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8bff7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8bff7-113">-Force</span><span class="sxs-lookup"><span data-stu-id="8bff7-113">-Force</span></span>
<span data-ttu-id="8bff7-114">Не запрашивать подтверждение, если вы хотите удалить ресурс</span><span class="sxs-lookup"><span data-stu-id="8bff7-114">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="8bff7-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8bff7-115">-Name</span></span>
<span data-ttu-id="8bff7-116">Имя группы безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="8bff7-116">The name of the application security group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bff7-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8bff7-117">-PassThru</span></span>
<span data-ttu-id="8bff7-118">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="8bff7-118">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="8bff7-119">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="8bff7-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8bff7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bff7-120">-ResourceGroupName</span></span>
<span data-ttu-id="8bff7-121">Имя группы ресурсов для группы безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="8bff7-121">The resource group name of the application security group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bff7-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8bff7-122">-Confirm</span></span>
<span data-ttu-id="8bff7-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8bff7-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bff7-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bff7-124">-WhatIf</span></span>
<span data-ttu-id="8bff7-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8bff7-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bff7-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8bff7-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bff7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bff7-127">CommonParameters</span></span>
<span data-ttu-id="8bff7-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8bff7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bff7-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bff7-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bff7-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8bff7-130">INPUTS</span></span>

### <span data-ttu-id="8bff7-131">System. String</span><span class="sxs-lookup"><span data-stu-id="8bff7-131">System.String</span></span>

## <span data-ttu-id="8bff7-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8bff7-132">OUTPUTS</span></span>

### <span data-ttu-id="8bff7-133">System. Object</span><span class="sxs-lookup"><span data-stu-id="8bff7-133">System.Object</span></span>

## <span data-ttu-id="8bff7-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="8bff7-134">NOTES</span></span>

## <span data-ttu-id="8bff7-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8bff7-135">RELATED LINKS</span></span>

[<span data-ttu-id="8bff7-136">New-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8bff7-136">New-AzureRmApplicationSecurityGroup</span></span>](./New-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="8bff7-137">Get-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8bff7-137">Get-AzureRmApplicationSecurityGroup</span></span>](./Get-AzureRmApplicationSecurityGroup.md)
