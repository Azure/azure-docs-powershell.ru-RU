---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: A87ED954-9C09-4329-A005-ABFF36C45E6E
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebApp.md
ms.openlocfilehash: d1217f3abc00fec8752fcddbb30e577df087b5de
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901761"
---
# <span data-ttu-id="a6c89-101">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a6c89-101">Get-AzWebApp</span></span>

## <span data-ttu-id="a6c89-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a6c89-102">SYNOPSIS</span></span>
<span data-ttu-id="a6c89-103">Получение веб-приложений Azure в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a6c89-103">Gets Azure Web Apps in the specified resource group.</span></span>

## <span data-ttu-id="a6c89-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a6c89-104">SYNTAX</span></span>

### <span data-ttu-id="a6c89-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="a6c89-105">S1</span></span>
```
Get-AzWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a6c89-106">S2</span><span class="sxs-lookup"><span data-stu-id="a6c89-106">S2</span></span>
```
Get-AzWebApp [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a6c89-107">Режима</span><span class="sxs-lookup"><span data-stu-id="a6c89-107">S3</span></span>
```
Get-AzWebApp [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6c89-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6c89-108">DESCRIPTION</span></span>
<span data-ttu-id="a6c89-109">Командлет **Get-AzWebApp** получает сведения о веб-приложении Azure.</span><span class="sxs-lookup"><span data-stu-id="a6c89-109">The **Get-AzWebApp** cmdlet gets information about an Azure Web App.</span></span>

## <span data-ttu-id="a6c89-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a6c89-110">EXAMPLES</span></span>

### <span data-ttu-id="a6c89-111">Пример 1: получение веб-приложения из группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="a6c89-111">Example 1: Get a Web App from a resource group</span></span>
```
PS C:\>Get-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="a6c89-112">Эта команда получает веб-приложение ContosoSite, которое принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="a6c89-112">This command gets the Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="a6c89-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a6c89-113">PARAMETERS</span></span>

### <span data-ttu-id="a6c89-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a6c89-114">-AppServicePlan</span></span>
<span data-ttu-id="a6c89-115">Объект плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="a6c89-115">App Service Plan object</span></span>

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

### <span data-ttu-id="a6c89-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6c89-116">-DefaultProfile</span></span>
<span data-ttu-id="a6c89-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a6c89-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6c89-118">-Location</span><span class="sxs-lookup"><span data-stu-id="a6c89-118">-Location</span></span>
<span data-ttu-id="a6c89-119">Поиска</span><span class="sxs-lookup"><span data-stu-id="a6c89-119">Location</span></span>

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

### <span data-ttu-id="a6c89-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a6c89-120">-Name</span></span>
<span data-ttu-id="a6c89-121">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="a6c89-121">WebApp Name</span></span>

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

### <span data-ttu-id="a6c89-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6c89-122">-ResourceGroupName</span></span>
<span data-ttu-id="a6c89-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="a6c89-123">Resource Group Name</span></span>

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

### <span data-ttu-id="a6c89-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6c89-124">CommonParameters</span></span>
<span data-ttu-id="a6c89-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a6c89-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6c89-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6c89-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6c89-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a6c89-127">INPUTS</span></span>

### <span data-ttu-id="a6c89-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a6c89-128">System.String</span></span>

## <span data-ttu-id="a6c89-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6c89-129">OUTPUTS</span></span>

### <span data-ttu-id="a6c89-130">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="a6c89-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="a6c89-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="a6c89-131">NOTES</span></span>

## <span data-ttu-id="a6c89-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a6c89-132">RELATED LINKS</span></span>

[<span data-ttu-id="a6c89-133">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a6c89-133">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="a6c89-134">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a6c89-134">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="a6c89-135">Restarting-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a6c89-135">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="a6c89-136">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a6c89-136">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="a6c89-137">Остановить-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a6c89-137">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


