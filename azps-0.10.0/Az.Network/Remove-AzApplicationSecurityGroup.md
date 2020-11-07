---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
ms.openlocfilehash: 1bdad35adef15c15c77753c77533f35cfaf945ea
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909517"
---
# <span data-ttu-id="8013f-101">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8013f-101">Remove-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="8013f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8013f-102">SYNOPSIS</span></span>
<span data-ttu-id="8013f-103">Удаляет группу безопасности приложений.</span><span class="sxs-lookup"><span data-stu-id="8013f-103">Removes an application security group.</span></span>

## <span data-ttu-id="8013f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8013f-104">SYNTAX</span></span>

```
Remove-AzApplicationSecurityGroup -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8013f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8013f-105">DESCRIPTION</span></span>
<span data-ttu-id="8013f-106">Командлет **Remove-AzApplicationSecurityGroup** удаляет группу безопасности приложений.</span><span class="sxs-lookup"><span data-stu-id="8013f-106">The **Remove-AzApplicationSecurityGroup** cmdlet removes an application security group.</span></span>

## <span data-ttu-id="8013f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8013f-107">EXAMPLES</span></span>

### <span data-ttu-id="8013f-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8013f-108">Example 1</span></span>
```
PS C:\>Remove-AzApplicationSecurityGroup -Name "MyApplicationSecurityGrouo" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="8013f-109">Эта команда удаляет группу безопасности приложений с именем MyApplicationSecurityGrouo в группе ресурсов с именем MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8013f-109">This command deletes an application security group named MyApplicationSecurityGrouo in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="8013f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8013f-110">PARAMETERS</span></span>

### <span data-ttu-id="8013f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8013f-111">-DefaultProfile</span></span>
<span data-ttu-id="8013f-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8013f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8013f-113">-Force</span><span class="sxs-lookup"><span data-stu-id="8013f-113">-Force</span></span>
<span data-ttu-id="8013f-114">Не запрашивать подтверждение, если вы хотите удалить ресурс</span><span class="sxs-lookup"><span data-stu-id="8013f-114">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="8013f-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8013f-115">-Name</span></span>
<span data-ttu-id="8013f-116">Имя группы безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="8013f-116">The name of the application security group.</span></span>

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

### <span data-ttu-id="8013f-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8013f-117">-PassThru</span></span>
<span data-ttu-id="8013f-118">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="8013f-118">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="8013f-119">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="8013f-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8013f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8013f-120">-ResourceGroupName</span></span>
<span data-ttu-id="8013f-121">Имя группы ресурсов для группы безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="8013f-121">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="8013f-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8013f-122">-Confirm</span></span>
<span data-ttu-id="8013f-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8013f-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8013f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8013f-124">-WhatIf</span></span>
<span data-ttu-id="8013f-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8013f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8013f-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8013f-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8013f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8013f-127">CommonParameters</span></span>
<span data-ttu-id="8013f-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8013f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8013f-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8013f-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8013f-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8013f-130">INPUTS</span></span>

### <span data-ttu-id="8013f-131">System. String</span><span class="sxs-lookup"><span data-stu-id="8013f-131">System.String</span></span>

## <span data-ttu-id="8013f-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8013f-132">OUTPUTS</span></span>

### <span data-ttu-id="8013f-133">System. Object</span><span class="sxs-lookup"><span data-stu-id="8013f-133">System.Object</span></span>

## <span data-ttu-id="8013f-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="8013f-134">NOTES</span></span>

## <span data-ttu-id="8013f-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8013f-135">RELATED LINKS</span></span>

[<span data-ttu-id="8013f-136">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8013f-136">New-AzApplicationSecurityGroup</span></span>](./New-AzApplicationSecurityGroup.md)

[<span data-ttu-id="8013f-137">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8013f-137">Get-AzApplicationSecurityGroup</span></span>](./Get-AzApplicationSecurityGroup.md)
