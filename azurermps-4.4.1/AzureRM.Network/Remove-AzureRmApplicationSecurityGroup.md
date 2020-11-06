---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationSecurityGroup.md
ms.openlocfilehash: b0387d10950073c4655c6e6015edc6957ae14edc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565237"
---
# <span data-ttu-id="9003a-101">Remove-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9003a-101">Remove-AzureRmApplicationSecurityGroup</span></span>

## <span data-ttu-id="9003a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9003a-102">SYNOPSIS</span></span>
<span data-ttu-id="9003a-103">Удаляет группу безопасности приложений.</span><span class="sxs-lookup"><span data-stu-id="9003a-103">Removes an application security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9003a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9003a-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationSecurityGroup -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9003a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9003a-105">DESCRIPTION</span></span>
<span data-ttu-id="9003a-106">Командлет **Remove-AzureRmApplicationSecurityGroup** удаляет группу безопасности приложений.</span><span class="sxs-lookup"><span data-stu-id="9003a-106">The **Remove-AzureRmApplicationSecurityGroup** cmdlet removes an application security group.</span></span>

## <span data-ttu-id="9003a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9003a-107">EXAMPLES</span></span>

### <span data-ttu-id="9003a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9003a-108">Example 1</span></span>
```
PS C:\>Remove-AzureRmApplicationSecurityGroup -Name "MyApplicationSecurityGrouo" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="9003a-109">Эта команда удаляет группу безопасности приложений с именем MyApplicationSecurityGrouo в группе ресурсов с именем MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="9003a-109">This command deletes an application security group named MyApplicationSecurityGrouo in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="9003a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9003a-110">PARAMETERS</span></span>

### <span data-ttu-id="9003a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9003a-111">-DefaultProfile</span></span>
<span data-ttu-id="9003a-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9003a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9003a-113">-Force</span><span class="sxs-lookup"><span data-stu-id="9003a-113">-Force</span></span>
<span data-ttu-id="9003a-114">Не запрашивать подтверждение, если вы хотите удалить ресурс</span><span class="sxs-lookup"><span data-stu-id="9003a-114">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="9003a-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9003a-115">-Name</span></span>
<span data-ttu-id="9003a-116">Имя группы безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="9003a-116">The name of the application security group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9003a-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9003a-117">-PassThru</span></span>
<span data-ttu-id="9003a-118">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="9003a-118">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="9003a-119">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="9003a-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9003a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9003a-120">-ResourceGroupName</span></span>
<span data-ttu-id="9003a-121">Имя группы ресурсов для группы безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="9003a-121">The resource group name of the application security group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9003a-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9003a-122">-Confirm</span></span>
<span data-ttu-id="9003a-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9003a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9003a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9003a-124">-WhatIf</span></span>
<span data-ttu-id="9003a-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9003a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9003a-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9003a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9003a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9003a-127">CommonParameters</span></span>
<span data-ttu-id="9003a-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9003a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9003a-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9003a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9003a-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9003a-130">INPUTS</span></span>

### <span data-ttu-id="9003a-131">System. String</span><span class="sxs-lookup"><span data-stu-id="9003a-131">System.String</span></span>

## <span data-ttu-id="9003a-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9003a-132">OUTPUTS</span></span>

### <span data-ttu-id="9003a-133">System. Object</span><span class="sxs-lookup"><span data-stu-id="9003a-133">System.Object</span></span>

## <span data-ttu-id="9003a-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="9003a-134">NOTES</span></span>

## <span data-ttu-id="9003a-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9003a-135">RELATED LINKS</span></span>

[<span data-ttu-id="9003a-136">New-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9003a-136">New-AzureRmApplicationSecurityGroup</span></span>](./New-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="9003a-137">Get-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9003a-137">Get-AzureRmApplicationSecurityGroup</span></span>](./Get-AzureRmApplicationSecurityGroup.md)
