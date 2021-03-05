---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzDeletedWebApp.md
ms.openlocfilehash: a67e48cdcad9d80d244e74ef8e20f81fcbd157cd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983891"
---
# <span data-ttu-id="6dad5-101">Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="6dad5-101">Get-AzDeletedWebApp</span></span>

## <span data-ttu-id="6dad5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6dad5-102">SYNOPSIS</span></span>
<span data-ttu-id="6dad5-103">Удаляется из подписки веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="6dad5-103">Gets deleted web apps in the subscription.</span></span>

## <span data-ttu-id="6dad5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6dad5-104">SYNTAX</span></span>

```
Get-AzDeletedWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [[-Slot] <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6dad5-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6dad5-105">DESCRIPTION</span></span>
<span data-ttu-id="6dad5-106">Для получения всех удаленных веб-приложений в подписке **возвращается cmdlet Get-AzDeletedWebApp.**</span><span class="sxs-lookup"><span data-stu-id="6dad5-106">The **Get-AzDeletedWebApp** cmdlet returns all deleted web apps in the subscription.</span></span> <span data-ttu-id="6dad5-107">При желании удаленные приложения можно отфильтровать по группе ресурсов, имени и слоту.</span><span class="sxs-lookup"><span data-stu-id="6dad5-107">Deleted apps can optionally be filtered by resource group, name, and slot.</span></span> <span data-ttu-id="6dad5-108">Может быть несколько удаленных приложений с одинаковыми именем и группой ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6dad5-108">There can be more than one deleted app with the same name and resource group.</span></span> <span data-ttu-id="6dad5-109">Проверьте DeletionTime, чтобы различать удаленные приложения с одинаковыми именами.</span><span class="sxs-lookup"><span data-stu-id="6dad5-109">Check the DeletionTime to distinguish deleted apps that share the same name.</span></span>

## <span data-ttu-id="6dad5-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6dad5-110">EXAMPLES</span></span>

### <span data-ttu-id="6dad5-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6dad5-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeletedWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="6dad5-112">Эта команда возвращает удаленные приложения ContosoSite, принадлежащие группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="6dad5-112">This command gets the deleted apps named ContosoSite belonging to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="6dad5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6dad5-113">PARAMETERS</span></span>

### <span data-ttu-id="6dad5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dad5-114">-DefaultProfile</span></span>
<span data-ttu-id="6dad5-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6dad5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6dad5-116">-Location</span><span class="sxs-lookup"><span data-stu-id="6dad5-116">-Location</span></span>
<span data-ttu-id="6dad5-117">Расположение удаленного приложения.</span><span class="sxs-lookup"><span data-stu-id="6dad5-117">The location of the deleted app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dad5-118">-Name</span><span class="sxs-lookup"><span data-stu-id="6dad5-118">-Name</span></span>
<span data-ttu-id="6dad5-119">Имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="6dad5-119">The name of the web app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dad5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6dad5-120">-ResourceGroupName</span></span>
<span data-ttu-id="6dad5-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6dad5-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dad5-122">-Slot</span><span class="sxs-lookup"><span data-stu-id="6dad5-122">-Slot</span></span>
<span data-ttu-id="6dad5-123">Название слота веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="6dad5-123">The name of the web app slot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dad5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dad5-124">CommonParameters</span></span>
<span data-ttu-id="6dad5-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6dad5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dad5-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6dad5-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dad5-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6dad5-127">INPUTS</span></span>

### <span data-ttu-id="6dad5-128">Нет</span><span class="sxs-lookup"><span data-stu-id="6dad5-128">None</span></span>

## <span data-ttu-id="6dad5-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6dad5-129">OUTPUTS</span></span>

### <span data-ttu-id="6dad5-130">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="6dad5-130">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="6dad5-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6dad5-131">NOTES</span></span>

## <span data-ttu-id="6dad5-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6dad5-132">RELATED LINKS</span></span>

[<span data-ttu-id="6dad5-133">Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="6dad5-133">Restore-AzDeletedWebApp</span></span>](./Restore-AzDeletedWebApp.md)