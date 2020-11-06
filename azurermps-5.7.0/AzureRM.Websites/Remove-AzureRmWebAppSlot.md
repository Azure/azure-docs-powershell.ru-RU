---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSlot.md
ms.openlocfilehash: eeaeb43083a2b125147df5d91516b71bdff377a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567860"
---
# <span data-ttu-id="56b2c-101">Remove-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="56b2c-101">Remove-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="56b2c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="56b2c-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56b2c-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="56b2c-103">SYNTAX</span></span>

### <span data-ttu-id="56b2c-104">Состояний</span><span class="sxs-lookup"><span data-stu-id="56b2c-104">S1</span></span>
```
Remove-AzureRmWebAppSlot [-Force] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56b2c-105">S2</span><span class="sxs-lookup"><span data-stu-id="56b2c-105">S2</span></span>
```
Remove-AzureRmWebAppSlot [-Force] [-WebApp] <Site> [-AsJob][-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56b2c-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="56b2c-106">DESCRIPTION</span></span>
<span data-ttu-id="56b2c-107">Командлет **Remove-AzureRmWebAppSlot** удаляет слот веб-приложения Azure, который предоставил группу ресурсов и имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="56b2c-107">The **Remove-AzureRmWebAppSlot** cmdlet removes an Azure Web App Slot provided the resource group and Web App name.</span></span>
<span data-ttu-id="56b2c-108">Этот командлет по умолчанию также удаляет все слоты и метрики.</span><span class="sxs-lookup"><span data-stu-id="56b2c-108">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="56b2c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="56b2c-109">EXAMPLES</span></span>

### <span data-ttu-id="56b2c-110">Пример 1: удаление слота веб-приложения</span><span class="sxs-lookup"><span data-stu-id="56b2c-110">Example 1: Remove a Web App Slot</span></span>
```
PS C:\>Remove-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -Slot "ContosoSlot"
```

<span data-ttu-id="56b2c-111">Эта команда удаляет гнездо с именем Slot001, связанное с ContosoSite веб-приложения, которое принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="56b2c-111">This command removes the Slot named Slot001 associated with Web App ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="56b2c-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="56b2c-112">PARAMETERS</span></span>

### <span data-ttu-id="56b2c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56b2c-113">-DefaultProfile</span></span>
<span data-ttu-id="56b2c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="56b2c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56b2c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="56b2c-115">-Force</span></span>
<span data-ttu-id="56b2c-116">Параметр принудительного удаления</span><span class="sxs-lookup"><span data-stu-id="56b2c-116">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="56b2c-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="56b2c-117">-Name</span></span>
<span data-ttu-id="56b2c-118">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="56b2c-118">WebApp Name</span></span>

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

### <span data-ttu-id="56b2c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56b2c-119">-ResourceGroupName</span></span>
<span data-ttu-id="56b2c-120">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="56b2c-120">Resource Group Name</span></span>

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

### <span data-ttu-id="56b2c-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="56b2c-121">-Slot</span></span>
<span data-ttu-id="56b2c-122">Название гнезда WebApp</span><span class="sxs-lookup"><span data-stu-id="56b2c-122">WebApp Slot Name</span></span>

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

### <span data-ttu-id="56b2c-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="56b2c-123">-WebApp</span></span>
<span data-ttu-id="56b2c-124">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="56b2c-124">WebApp Object</span></span>

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

### <span data-ttu-id="56b2c-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="56b2c-125">-Confirm</span></span>
<span data-ttu-id="56b2c-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="56b2c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56b2c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56b2c-127">-WhatIf</span></span>
<span data-ttu-id="56b2c-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="56b2c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56b2c-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="56b2c-129">The cmdlet is not run.</span></span>

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
### <span data-ttu-id="56b2c-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="56b2c-130">-AsJob</span></span>
<span data-ttu-id="56b2c-131">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="56b2c-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="56b2c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56b2c-132">CommonParameters</span></span>
<span data-ttu-id="56b2c-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="56b2c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56b2c-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56b2c-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56b2c-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="56b2c-135">INPUTS</span></span>

### <span data-ttu-id="56b2c-136">Семейств</span><span class="sxs-lookup"><span data-stu-id="56b2c-136">Site</span></span>
<span data-ttu-id="56b2c-137">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="56b2c-137">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="56b2c-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="56b2c-138">OUTPUTS</span></span>

### <span data-ttu-id="56b2c-139">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="56b2c-139">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="56b2c-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="56b2c-140">NOTES</span></span>

## <span data-ttu-id="56b2c-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="56b2c-141">RELATED LINKS</span></span>

[<span data-ttu-id="56b2c-142">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="56b2c-142">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="56b2c-143">New-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="56b2c-143">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="56b2c-144">Restarting-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="56b2c-144">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="56b2c-145">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="56b2c-145">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="56b2c-146">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="56b2c-146">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="56b2c-147">Остановить-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="56b2c-147">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="56b2c-148">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="56b2c-148">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
