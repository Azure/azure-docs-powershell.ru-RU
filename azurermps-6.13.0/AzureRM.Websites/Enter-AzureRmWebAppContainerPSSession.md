---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/?view=azurermps-6.8.1
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Enter-AzureRmWebAppContainerPSSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Enter-AzureRmWebAppContainerPSSession.md
ms.openlocfilehash: 350ad76952a2953a107e0626b9cf2e0e8b640bb3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558127"
---
# <span data-ttu-id="96a8e-101">Enter-AzureRmWebAppContainerPSSession</span><span class="sxs-lookup"><span data-stu-id="96a8e-101">Enter-AzureRmWebAppContainerPSSession</span></span>

## <span data-ttu-id="96a8e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="96a8e-102">SYNOPSIS</span></span>
<span data-ttu-id="96a8e-103">Открытие удаленного сеанса PowerShell в контейнере Windows, указанном на данном сайте или в области, и данной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="96a8e-103">Opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96a8e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="96a8e-104">SYNTAX</span></span>

### <span data-ttu-id="96a8e-105">S1 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="96a8e-105">S1 (Default)</span></span>
```
Enter-AzureRmWebAppContainerPSSession [-PassThru] [-Force] [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96a8e-106">S2</span><span class="sxs-lookup"><span data-stu-id="96a8e-106">S2</span></span>
```
Enter-AzureRmWebAppContainerPSSession [-PassThru] [-Force] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96a8e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="96a8e-107">DESCRIPTION</span></span>
<span data-ttu-id="96a8e-108">открытие удаленного сеанса PowerShell в контейнере Windows, указанном на данном сайте или в области, и данной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="96a8e-108">opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="96a8e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="96a8e-109">EXAMPLES</span></span>

### <span data-ttu-id="96a8e-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="96a8e-110">Example 1</span></span>
```
PS C:\> Enter-AzureRmWebAppContainerPSSession -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="96a8e-111">Эта команда открывает удаленный сеанс PowerShell в приложении контейнера Windows ContosoASP</span><span class="sxs-lookup"><span data-stu-id="96a8e-111">This command opens a remote PowerShell session into the windows container app ContosoASP</span></span>

## <span data-ttu-id="96a8e-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="96a8e-112">PARAMETERS</span></span>

### <span data-ttu-id="96a8e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96a8e-113">-DefaultProfile</span></span>
<span data-ttu-id="96a8e-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="96a8e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96a8e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="96a8e-115">-Force</span></span>
<span data-ttu-id="96a8e-116">Создайте сеанс PowerShell без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="96a8e-116">Create the PowerShell session without prompting for confirmation.</span></span>

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

### <span data-ttu-id="96a8e-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="96a8e-117">-Name</span></span>
<span data-ttu-id="96a8e-118">Имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="96a8e-118">The name of the web app.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96a8e-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="96a8e-119">-PassThru</span></span>
<span data-ttu-id="96a8e-120">Возвращение значения, показывающего успешное выполнение или сбой</span><span class="sxs-lookup"><span data-stu-id="96a8e-120">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="96a8e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96a8e-121">-ResourceGroupName</span></span>
<span data-ttu-id="96a8e-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="96a8e-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96a8e-123">-SlotName</span><span class="sxs-lookup"><span data-stu-id="96a8e-123">-SlotName</span></span>
<span data-ttu-id="96a8e-124">Имя области веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="96a8e-124">The name of the web app slot.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96a8e-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="96a8e-125">-WebApp</span></span>
<span data-ttu-id="96a8e-126">Объект веб-приложения</span><span class="sxs-lookup"><span data-stu-id="96a8e-126">The web app object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96a8e-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="96a8e-127">-Confirm</span></span>
<span data-ttu-id="96a8e-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="96a8e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96a8e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96a8e-129">-WhatIf</span></span>
<span data-ttu-id="96a8e-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="96a8e-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="96a8e-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="96a8e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96a8e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96a8e-132">CommonParameters</span></span>
<span data-ttu-id="96a8e-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="96a8e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96a8e-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96a8e-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96a8e-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="96a8e-135">INPUTS</span></span>

### <span data-ttu-id="96a8e-136">System. String</span><span class="sxs-lookup"><span data-stu-id="96a8e-136">System.String</span></span>
### <span data-ttu-id="96a8e-137">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="96a8e-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>
## <span data-ttu-id="96a8e-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="96a8e-138">OUTPUTS</span></span>

### <span data-ttu-id="96a8e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="96a8e-139">System.String</span></span>
## <span data-ttu-id="96a8e-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="96a8e-140">NOTES</span></span>

## <span data-ttu-id="96a8e-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="96a8e-141">RELATED LINKS</span></span>
