---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: A87ED954-9C09-4329-A005-ABFF36C45E6E
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebApp.md
ms.openlocfilehash: 7dc1d2c5d6be1fd920ec9fb4eb90bf73b2c464b9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243128"
---
# <span data-ttu-id="1f6f6-101">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1f6f6-101">Get-AzWebApp</span></span>

## <span data-ttu-id="1f6f6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1f6f6-102">SYNOPSIS</span></span>
<span data-ttu-id="1f6f6-103">Получение веб-приложений Azure в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1f6f6-103">Gets Azure Web Apps in the specified resource group.</span></span>

## <span data-ttu-id="1f6f6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1f6f6-104">SYNTAX</span></span>

### <span data-ttu-id="1f6f6-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="1f6f6-105">S1</span></span>
```
Get-AzWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1f6f6-106">S2</span><span class="sxs-lookup"><span data-stu-id="1f6f6-106">S2</span></span>
```
Get-AzWebApp [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1f6f6-107">Режима</span><span class="sxs-lookup"><span data-stu-id="1f6f6-107">S3</span></span>
```
Get-AzWebApp [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f6f6-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f6f6-108">DESCRIPTION</span></span>
<span data-ttu-id="1f6f6-109">Командлет **Get-AzWebApp** получает сведения о веб-приложении Azure.</span><span class="sxs-lookup"><span data-stu-id="1f6f6-109">The **Get-AzWebApp** cmdlet gets information about an Azure Web App.</span></span>

## <span data-ttu-id="1f6f6-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1f6f6-110">EXAMPLES</span></span>

### <span data-ttu-id="1f6f6-111">Пример 1: получение веб-приложения из группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="1f6f6-111">Example 1: Get a Web App from a resource group</span></span>
```
PS C:\>Get-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="1f6f6-112">Эта команда получает веб-приложение ContosoSite, которое принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="1f6f6-112">This command gets the Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="1f6f6-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1f6f6-113">PARAMETERS</span></span>

### <span data-ttu-id="1f6f6-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="1f6f6-114">-AppServicePlan</span></span>
<span data-ttu-id="1f6f6-115">Объект плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="1f6f6-115">App Service Plan object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f6f6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f6f6-116">-DefaultProfile</span></span>
<span data-ttu-id="1f6f6-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1f6f6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f6f6-118">-Location</span><span class="sxs-lookup"><span data-stu-id="1f6f6-118">-Location</span></span>
<span data-ttu-id="1f6f6-119">Поиска</span><span class="sxs-lookup"><span data-stu-id="1f6f6-119">Location</span></span>

```yaml
Type: System.String
Parameter Sets: S3
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f6f6-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1f6f6-120">-Name</span></span>
<span data-ttu-id="1f6f6-121">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="1f6f6-121">WebApp Name</span></span>

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

### <span data-ttu-id="1f6f6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f6f6-122">-ResourceGroupName</span></span>
<span data-ttu-id="1f6f6-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="1f6f6-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f6f6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f6f6-124">CommonParameters</span></span>
<span data-ttu-id="1f6f6-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1f6f6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f6f6-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f6f6-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f6f6-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1f6f6-127">INPUTS</span></span>

### <span data-ttu-id="1f6f6-128">System. String</span><span class="sxs-lookup"><span data-stu-id="1f6f6-128">System.String</span></span>

## <span data-ttu-id="1f6f6-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f6f6-129">OUTPUTS</span></span>

### <span data-ttu-id="1f6f6-130">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="1f6f6-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="1f6f6-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="1f6f6-131">NOTES</span></span>

## <span data-ttu-id="1f6f6-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1f6f6-132">RELATED LINKS</span></span>

[<span data-ttu-id="1f6f6-133">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1f6f6-133">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="1f6f6-134">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1f6f6-134">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="1f6f6-135">Restarting-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1f6f6-135">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="1f6f6-136">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1f6f6-136">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="1f6f6-137">Остановить-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1f6f6-137">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


