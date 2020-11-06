---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmDeletedWebApp.md
ms.openlocfilehash: 75ad4e1fabb511ee4ca3cff024389a8e826aeadd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565295"
---
# <span data-ttu-id="aa3ac-101">Get-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="aa3ac-101">Get-AzureRmDeletedWebApp</span></span>

## <span data-ttu-id="aa3ac-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aa3ac-102">SYNOPSIS</span></span>
<span data-ttu-id="aa3ac-103">Получает удаление веб-приложений в подписке.</span><span class="sxs-lookup"><span data-stu-id="aa3ac-103">Gets deleted web apps in the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa3ac-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aa3ac-104">SYNTAX</span></span>

```
Get-AzureRmDeletedWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa3ac-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa3ac-105">DESCRIPTION</span></span>
<span data-ttu-id="aa3ac-106">Командлет **Get-AzureRmDeletedWebApp** возвращает все удаленные веб-приложения в подписке.</span><span class="sxs-lookup"><span data-stu-id="aa3ac-106">The **Get-AzureRmDeletedWebApp** cmdlet returns all deleted web apps in the subscription.</span></span> <span data-ttu-id="aa3ac-107">Удаленные приложения можно дополнительно отфильтровать по группам ресурсов, именам и ячейкам.</span><span class="sxs-lookup"><span data-stu-id="aa3ac-107">Deleted apps can optionally be filtered by resource group, name, and slot.</span></span> <span data-ttu-id="aa3ac-108">Может быть несколько удаленных приложений с одинаковыми именами и группами ресурсов.</span><span class="sxs-lookup"><span data-stu-id="aa3ac-108">There can be more than one deleted app with the same name and resource group.</span></span> <span data-ttu-id="aa3ac-109">Проверьте DeletionTime, чтобы отличать удаленные приложения, которые имеют одно и то же имя.</span><span class="sxs-lookup"><span data-stu-id="aa3ac-109">Check the DeletionTime to distinguish deleted apps that share the same name.</span></span>

## <span data-ttu-id="aa3ac-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aa3ac-110">EXAMPLES</span></span>

### <span data-ttu-id="aa3ac-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="aa3ac-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDeletedWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="aa3ac-112">Эта команда получает удаленные приложения с именем ContosoSite, которые принадлежат группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="aa3ac-112">This command gets the deleted apps named ContosoSite belonging to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="aa3ac-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aa3ac-113">PARAMETERS</span></span>

### <span data-ttu-id="aa3ac-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa3ac-114">-DefaultProfile</span></span>
<span data-ttu-id="aa3ac-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aa3ac-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa3ac-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="aa3ac-116">-Name</span></span>
<span data-ttu-id="aa3ac-117">Имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="aa3ac-117">The name of the web app.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa3ac-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa3ac-118">-ResourceGroupName</span></span>
<span data-ttu-id="aa3ac-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="aa3ac-119">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa3ac-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="aa3ac-120">-Slot</span></span>
<span data-ttu-id="aa3ac-121">Имя области веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="aa3ac-121">The name of the web app slot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa3ac-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa3ac-122">CommonParameters</span></span>
<span data-ttu-id="aa3ac-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aa3ac-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="aa3ac-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa3ac-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa3ac-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aa3ac-125">INPUTS</span></span>

### <span data-ttu-id="aa3ac-126">Ничего</span><span class="sxs-lookup"><span data-stu-id="aa3ac-126">None</span></span>

## <span data-ttu-id="aa3ac-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa3ac-127">OUTPUTS</span></span>

### <span data-ttu-id="aa3ac-128">Microsoft. Azure. Commands. Apps. командлеты. PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="aa3ac-128">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="aa3ac-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="aa3ac-129">NOTES</span></span>

## <span data-ttu-id="aa3ac-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aa3ac-130">RELATED LINKS</span></span>

[<span data-ttu-id="aa3ac-131">Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="aa3ac-131">Restore-AzureRmDeletedWebApp</span></span>](./Restore-AzureRmDeletedWebApp.md)
