---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzDeletedWebApp.md
ms.openlocfilehash: 74c518d4713c19c7a1bb7b7d0b3341e164e22c35
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327140"
---
# <span data-ttu-id="95175-101">Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="95175-101">Get-AzDeletedWebApp</span></span>

## <span data-ttu-id="95175-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95175-102">SYNOPSIS</span></span>
<span data-ttu-id="95175-103">Удаляется из подписки веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="95175-103">Gets deleted web apps in the subscription.</span></span>

## <span data-ttu-id="95175-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="95175-104">SYNTAX</span></span>

```
Get-AzDeletedWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [[-Slot] <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95175-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="95175-105">DESCRIPTION</span></span>
<span data-ttu-id="95175-106">Для получения всех удаленных веб-приложений в подписке **возвращается cmdlet Get-AzDeletedWebApp.**</span><span class="sxs-lookup"><span data-stu-id="95175-106">The **Get-AzDeletedWebApp** cmdlet returns all deleted web apps in the subscription.</span></span> <span data-ttu-id="95175-107">При желании удаленные приложения можно отфильтровать по группе ресурсов, имени и слоту.</span><span class="sxs-lookup"><span data-stu-id="95175-107">Deleted apps can optionally be filtered by resource group, name, and slot.</span></span> <span data-ttu-id="95175-108">Может быть несколько удаленных приложений с одинаковыми именем и группой ресурсов.</span><span class="sxs-lookup"><span data-stu-id="95175-108">There can be more than one deleted app with the same name and resource group.</span></span> <span data-ttu-id="95175-109">Проверьте DeletionTime, чтобы различать удаленные приложения с одинаковыми именами.</span><span class="sxs-lookup"><span data-stu-id="95175-109">Check the DeletionTime to distinguish deleted apps that share the same name.</span></span>

## <span data-ttu-id="95175-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="95175-110">EXAMPLES</span></span>

### <span data-ttu-id="95175-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="95175-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeletedWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="95175-112">Эта команда возвращает удаленные приложения ContosoSite, принадлежащие группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="95175-112">This command gets the deleted apps named ContosoSite belonging to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="95175-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="95175-113">PARAMETERS</span></span>

### <span data-ttu-id="95175-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95175-114">-DefaultProfile</span></span>
<span data-ttu-id="95175-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="95175-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95175-116">-Location</span><span class="sxs-lookup"><span data-stu-id="95175-116">-Location</span></span>
<span data-ttu-id="95175-117">Расположение удаленного приложения.</span><span class="sxs-lookup"><span data-stu-id="95175-117">The location of the deleted app.</span></span>

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

### <span data-ttu-id="95175-118">-Name</span><span class="sxs-lookup"><span data-stu-id="95175-118">-Name</span></span>
<span data-ttu-id="95175-119">Имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="95175-119">The name of the web app.</span></span>

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

### <span data-ttu-id="95175-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95175-120">-ResourceGroupName</span></span>
<span data-ttu-id="95175-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="95175-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="95175-122">-Slot</span><span class="sxs-lookup"><span data-stu-id="95175-122">-Slot</span></span>
<span data-ttu-id="95175-123">Название слота веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="95175-123">The name of the web app slot.</span></span>

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

### <span data-ttu-id="95175-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95175-124">CommonParameters</span></span>
<span data-ttu-id="95175-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95175-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95175-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95175-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95175-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="95175-127">INPUTS</span></span>

### <span data-ttu-id="95175-128">Нет</span><span class="sxs-lookup"><span data-stu-id="95175-128">None</span></span>

## <span data-ttu-id="95175-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="95175-129">OUTPUTS</span></span>

### <span data-ttu-id="95175-130">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="95175-130">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="95175-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="95175-131">NOTES</span></span>

## <span data-ttu-id="95175-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="95175-132">RELATED LINKS</span></span>

[<span data-ttu-id="95175-133">Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="95175-133">Restore-AzDeletedWebApp</span></span>](./Restore-AzDeletedWebApp.md)