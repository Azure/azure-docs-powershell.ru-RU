---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/remove-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzWebAppSlot.md
ms.openlocfilehash: 04813b04d3d2499de549655edb6398550ce25536
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910584"
---
# <span data-ttu-id="84515-101">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="84515-101">Remove-AzWebAppSlot</span></span>

## <span data-ttu-id="84515-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="84515-102">SYNOPSIS</span></span>

## <span data-ttu-id="84515-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="84515-103">SYNTAX</span></span>

### <span data-ttu-id="84515-104">Состояний</span><span class="sxs-lookup"><span data-stu-id="84515-104">S1</span></span>
```
Remove-AzWebAppSlot [-Force] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84515-105">S2</span><span class="sxs-lookup"><span data-stu-id="84515-105">S2</span></span>
```
Remove-AzWebAppSlot [-Force] [-WebApp] <Site> [-AsJob][-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84515-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="84515-106">DESCRIPTION</span></span>
<span data-ttu-id="84515-107">Командлет **Remove-AzWebAppSlot** удаляет слот веб-приложения Azure, который предоставил группу ресурсов и имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="84515-107">The **Remove-AzWebAppSlot** cmdlet removes an Azure Web App Slot provided the resource group and Web App name.</span></span>
<span data-ttu-id="84515-108">Этот командлет по умолчанию также удаляет все слоты и метрики.</span><span class="sxs-lookup"><span data-stu-id="84515-108">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="84515-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="84515-109">EXAMPLES</span></span>

### <span data-ttu-id="84515-110">Пример 1: удаление слота веб-приложения</span><span class="sxs-lookup"><span data-stu-id="84515-110">Example 1: Remove a Web App Slot</span></span>
```
PS C:\>Remove-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -Slot "ContosoSlot"
```

<span data-ttu-id="84515-111">Эта команда удаляет гнездо с именем Slot001, связанное с ContosoSite веб-приложения, которое принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="84515-111">This command removes the Slot named Slot001 associated with Web App ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="84515-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="84515-112">PARAMETERS</span></span>

### <span data-ttu-id="84515-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84515-113">-DefaultProfile</span></span>
<span data-ttu-id="84515-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="84515-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84515-115">-Force</span><span class="sxs-lookup"><span data-stu-id="84515-115">-Force</span></span>
<span data-ttu-id="84515-116">Параметр принудительного удаления</span><span class="sxs-lookup"><span data-stu-id="84515-116">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="84515-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="84515-117">-Name</span></span>
<span data-ttu-id="84515-118">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="84515-118">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84515-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84515-119">-ResourceGroupName</span></span>
<span data-ttu-id="84515-120">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="84515-120">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84515-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="84515-121">-Slot</span></span>
<span data-ttu-id="84515-122">Название гнезда WebApp</span><span class="sxs-lookup"><span data-stu-id="84515-122">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84515-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="84515-123">-WebApp</span></span>
<span data-ttu-id="84515-124">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="84515-124">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84515-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="84515-125">-Confirm</span></span>
<span data-ttu-id="84515-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="84515-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84515-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84515-127">-WhatIf</span></span>
<span data-ttu-id="84515-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="84515-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84515-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="84515-129">The cmdlet is not run.</span></span>

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
### <span data-ttu-id="84515-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="84515-130">-AsJob</span></span>
<span data-ttu-id="84515-131">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="84515-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="84515-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84515-132">CommonParameters</span></span>
<span data-ttu-id="84515-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="84515-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84515-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84515-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84515-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="84515-135">INPUTS</span></span>

### <span data-ttu-id="84515-136">Семейств</span><span class="sxs-lookup"><span data-stu-id="84515-136">Site</span></span>
<span data-ttu-id="84515-137">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="84515-137">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="84515-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="84515-138">OUTPUTS</span></span>

### <span data-ttu-id="84515-139">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="84515-139">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="84515-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="84515-140">NOTES</span></span>

## <span data-ttu-id="84515-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="84515-141">RELATED LINKS</span></span>

[<span data-ttu-id="84515-142">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="84515-142">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="84515-143">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="84515-143">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="84515-144">Restarting-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="84515-144">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="84515-145">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="84515-145">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="84515-146">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="84515-146">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="84515-147">Остановить-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="84515-147">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="84515-148">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="84515-148">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
