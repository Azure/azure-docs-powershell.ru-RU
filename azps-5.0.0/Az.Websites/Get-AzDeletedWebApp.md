---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzDeletedWebApp.md
ms.openlocfilehash: 74c518d4713c19c7a1bb7b7d0b3341e164e22c35
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249930"
---
# <span data-ttu-id="f797a-101">Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="f797a-101">Get-AzDeletedWebApp</span></span>

## <span data-ttu-id="f797a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f797a-102">SYNOPSIS</span></span>
<span data-ttu-id="f797a-103">Получает удаление веб-приложений в подписке.</span><span class="sxs-lookup"><span data-stu-id="f797a-103">Gets deleted web apps in the subscription.</span></span>

## <span data-ttu-id="f797a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f797a-104">SYNTAX</span></span>

```
Get-AzDeletedWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [[-Slot] <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f797a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f797a-105">DESCRIPTION</span></span>
<span data-ttu-id="f797a-106">Командлет **Get-AzDeletedWebApp** возвращает все удаленные веб-приложения в подписке.</span><span class="sxs-lookup"><span data-stu-id="f797a-106">The **Get-AzDeletedWebApp** cmdlet returns all deleted web apps in the subscription.</span></span> <span data-ttu-id="f797a-107">Удаленные приложения можно дополнительно отфильтровать по группам ресурсов, именам и ячейкам.</span><span class="sxs-lookup"><span data-stu-id="f797a-107">Deleted apps can optionally be filtered by resource group, name, and slot.</span></span> <span data-ttu-id="f797a-108">Может быть несколько удаленных приложений с одинаковыми именами и группами ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f797a-108">There can be more than one deleted app with the same name and resource group.</span></span> <span data-ttu-id="f797a-109">Проверьте DeletionTime, чтобы отличать удаленные приложения, которые имеют одно и то же имя.</span><span class="sxs-lookup"><span data-stu-id="f797a-109">Check the DeletionTime to distinguish deleted apps that share the same name.</span></span>

## <span data-ttu-id="f797a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f797a-110">EXAMPLES</span></span>

### <span data-ttu-id="f797a-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f797a-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeletedWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="f797a-112">Эта команда получает удаленные приложения с именем ContosoSite, которые принадлежат группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="f797a-112">This command gets the deleted apps named ContosoSite belonging to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="f797a-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f797a-113">PARAMETERS</span></span>

### <span data-ttu-id="f797a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f797a-114">-DefaultProfile</span></span>
<span data-ttu-id="f797a-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f797a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f797a-116">-Location</span><span class="sxs-lookup"><span data-stu-id="f797a-116">-Location</span></span>
<span data-ttu-id="f797a-117">Расположение удаленного приложения.</span><span class="sxs-lookup"><span data-stu-id="f797a-117">The location of the deleted app.</span></span>

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

### <span data-ttu-id="f797a-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f797a-118">-Name</span></span>
<span data-ttu-id="f797a-119">Имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="f797a-119">The name of the web app.</span></span>

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

### <span data-ttu-id="f797a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f797a-120">-ResourceGroupName</span></span>
<span data-ttu-id="f797a-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f797a-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="f797a-122">-Slot</span><span class="sxs-lookup"><span data-stu-id="f797a-122">-Slot</span></span>
<span data-ttu-id="f797a-123">Имя области веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="f797a-123">The name of the web app slot.</span></span>

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

### <span data-ttu-id="f797a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f797a-124">CommonParameters</span></span>
<span data-ttu-id="f797a-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f797a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f797a-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f797a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f797a-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f797a-127">INPUTS</span></span>

### <span data-ttu-id="f797a-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="f797a-128">None</span></span>

## <span data-ttu-id="f797a-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f797a-129">OUTPUTS</span></span>

### <span data-ttu-id="f797a-130">Microsoft. Azure. Commands. Apps. командлеты. PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="f797a-130">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="f797a-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="f797a-131">NOTES</span></span>

## <span data-ttu-id="f797a-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f797a-132">RELATED LINKS</span></span>

[<span data-ttu-id="f797a-133">Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="f797a-133">Restore-AzDeletedWebApp</span></span>](./Restore-AzDeletedWebApp.md)