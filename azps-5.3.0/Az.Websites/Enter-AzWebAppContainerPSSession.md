---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/enter-azwebappcontainerpssession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Enter-AzWebAppContainerPSSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Enter-AzWebAppContainerPSSession.md
ms.openlocfilehash: ddf728a1340d763c1feb2ba313a2dc73494b5d30
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505798"
---
# <span data-ttu-id="724f6-101">Enter-AzWebAppContainerPSSession</span><span class="sxs-lookup"><span data-stu-id="724f6-101">Enter-AzWebAppContainerPSSession</span></span>

## <span data-ttu-id="724f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="724f6-102">SYNOPSIS</span></span>
<span data-ttu-id="724f6-103">Открытие удаленного сеанса PowerShell в контейнере Windows, указанном на определенном сайте или в слоте и заданной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="724f6-103">Opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="724f6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="724f6-104">SYNTAX</span></span>

### <span data-ttu-id="724f6-105">S1 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="724f6-105">S1 (Default)</span></span>
```
Enter-AzWebAppContainerPSSession [-PassThru] [-Force] [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="724f6-106">S2</span><span class="sxs-lookup"><span data-stu-id="724f6-106">S2</span></span>
```
Enter-AzWebAppContainerPSSession [-PassThru] [-Force] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="724f6-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="724f6-107">DESCRIPTION</span></span>
<span data-ttu-id="724f6-108">Открывает удаленный сеанс PowerShell в контейнере Windows, указанном на определенном сайте или в слоте и заданной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="724f6-108">opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="724f6-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="724f6-109">EXAMPLES</span></span>

### <span data-ttu-id="724f6-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="724f6-110">Example 1</span></span>
```
PS C:\> Enter-AzWebAppContainerPSSession -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="724f6-111">Эта команда открывает удаленный сеанс PowerShell в приложении contosoASP контейнера Windows</span><span class="sxs-lookup"><span data-stu-id="724f6-111">This command opens a remote PowerShell session into the windows container app ContosoASP</span></span>

## <span data-ttu-id="724f6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="724f6-112">PARAMETERS</span></span>

### <span data-ttu-id="724f6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="724f6-113">-DefaultProfile</span></span>
<span data-ttu-id="724f6-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="724f6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="724f6-115">-Force</span><span class="sxs-lookup"><span data-stu-id="724f6-115">-Force</span></span>
<span data-ttu-id="724f6-116">Создайте сеанс PowerShell без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="724f6-116">Create the PowerShell session without prompting for confirmation.</span></span>

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

### <span data-ttu-id="724f6-117">-Name</span><span class="sxs-lookup"><span data-stu-id="724f6-117">-Name</span></span>
<span data-ttu-id="724f6-118">Имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="724f6-118">The name of the web app.</span></span>

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

### <span data-ttu-id="724f6-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="724f6-119">-PassThru</span></span>
<span data-ttu-id="724f6-120">Возвращает значение, указывающее на успех или неудачу.</span><span class="sxs-lookup"><span data-stu-id="724f6-120">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="724f6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="724f6-121">-ResourceGroupName</span></span>
<span data-ttu-id="724f6-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="724f6-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="724f6-123">-SlotName</span><span class="sxs-lookup"><span data-stu-id="724f6-123">-SlotName</span></span>
<span data-ttu-id="724f6-124">Название слота веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="724f6-124">The name of the web app slot.</span></span>

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

### <span data-ttu-id="724f6-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="724f6-125">-WebApp</span></span>
<span data-ttu-id="724f6-126">Объект веб-приложения</span><span class="sxs-lookup"><span data-stu-id="724f6-126">The web app object</span></span>

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

### <span data-ttu-id="724f6-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="724f6-127">-Confirm</span></span>
<span data-ttu-id="724f6-128">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="724f6-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="724f6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="724f6-129">-WhatIf</span></span>
<span data-ttu-id="724f6-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="724f6-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="724f6-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="724f6-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="724f6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="724f6-132">CommonParameters</span></span>
<span data-ttu-id="724f6-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="724f6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="724f6-134">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="724f6-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="724f6-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="724f6-135">INPUTS</span></span>

### <span data-ttu-id="724f6-136">System.String</span><span class="sxs-lookup"><span data-stu-id="724f6-136">System.String</span></span>

### <span data-ttu-id="724f6-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="724f6-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="724f6-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="724f6-138">OUTPUTS</span></span>

### <span data-ttu-id="724f6-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="724f6-139">System.Void</span></span>

## <span data-ttu-id="724f6-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="724f6-140">NOTES</span></span>

## <span data-ttu-id="724f6-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="724f6-141">RELATED LINKS</span></span>
