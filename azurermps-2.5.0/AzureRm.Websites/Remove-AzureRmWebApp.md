---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermwebapp
schema: 2.0.0
ms.openlocfilehash: e7c0d37dc56e1ff4c986aa66632dccddec283c83
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914678"
---
# <span data-ttu-id="f8fb4-101">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f8fb4-101">Remove-AzureRmWebApp</span></span>

## <span data-ttu-id="f8fb4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f8fb4-102">SYNOPSIS</span></span>
<span data-ttu-id="f8fb4-103">Удаление веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="f8fb4-103">Removes an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8fb4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f8fb4-104">SYNTAX</span></span>

### <span data-ttu-id="f8fb4-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="f8fb4-105">S1</span></span>
```
Remove-AzureRmWebApp [-Force] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8fb4-106">S2</span><span class="sxs-lookup"><span data-stu-id="f8fb4-106">S2</span></span>
```
Remove-AzureRmWebApp [-Force] [-WebApp] <Site> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f8fb4-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f8fb4-107">DESCRIPTION</span></span>
<span data-ttu-id="f8fb4-108">Командлет **Remove-AzureRmWebApp** удаляет веб-приложение Azure, которое предоставил группу ресурсов и имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="f8fb4-108">The **Remove-AzureRmWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="f8fb4-109">Этот командлет по умолчанию также удаляет все слоты и метрики.</span><span class="sxs-lookup"><span data-stu-id="f8fb4-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="f8fb4-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f8fb4-110">EXAMPLES</span></span>

### <span data-ttu-id="f8fb4-111">Пример 1: удаление веб-приложения</span><span class="sxs-lookup"><span data-stu-id="f8fb4-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="f8fb4-112">Эта команда удаляет веб-приложение Azure с именем ContosoSite, которое принадлежит группе ресурсов с именем Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="f8fb4-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="f8fb4-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f8fb4-113">PARAMETERS</span></span>

### <span data-ttu-id="f8fb4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8fb4-114">-DefaultProfile</span></span>
<span data-ttu-id="f8fb4-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f8fb4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8fb4-116">-Force</span><span class="sxs-lookup"><span data-stu-id="f8fb4-116">-Force</span></span>
<span data-ttu-id="f8fb4-117">Параметр принудительного удаления</span><span class="sxs-lookup"><span data-stu-id="f8fb4-117">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="f8fb4-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f8fb4-118">-Name</span></span>
<span data-ttu-id="f8fb4-119">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="f8fb4-119">WebApp Name</span></span>

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

### <span data-ttu-id="f8fb4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8fb4-120">-ResourceGroupName</span></span>
<span data-ttu-id="f8fb4-121">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f8fb4-121">Resource Group Name</span></span>

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

### <span data-ttu-id="f8fb4-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="f8fb4-122">-WebApp</span></span>
<span data-ttu-id="f8fb4-123">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="f8fb4-123">WebApp Object</span></span>

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

### <span data-ttu-id="f8fb4-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f8fb4-124">-Confirm</span></span>
<span data-ttu-id="f8fb4-125">Запрашивает подтверждение перед запуском командлета. Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f8fb4-125">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8fb4-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8fb4-126">-WhatIf</span></span>
<span data-ttu-id="f8fb4-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f8fb4-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8fb4-128">Командлет не выполняется. Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f8fb4-128">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8fb4-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f8fb4-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8fb4-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f8fb4-130">-AsJob</span></span>
<span data-ttu-id="f8fb4-131">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f8fb4-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f8fb4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8fb4-132">CommonParameters</span></span>
<span data-ttu-id="f8fb4-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f8fb4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8fb4-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8fb4-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8fb4-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f8fb4-135">INPUTS</span></span>

### <span data-ttu-id="f8fb4-136">Семейств</span><span class="sxs-lookup"><span data-stu-id="f8fb4-136">Site</span></span>
<span data-ttu-id="f8fb4-137">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="f8fb4-137">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="f8fb4-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f8fb4-138">OUTPUTS</span></span>

## <span data-ttu-id="f8fb4-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="f8fb4-139">NOTES</span></span>

## <span data-ttu-id="f8fb4-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f8fb4-140">RELATED LINKS</span></span>

[<span data-ttu-id="f8fb4-141">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f8fb4-141">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="f8fb4-142">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f8fb4-142">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="f8fb4-143">Restarting-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f8fb4-143">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="f8fb4-144">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f8fb4-144">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="f8fb4-145">Остановить-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f8fb4-145">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


