---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: A87ED954-9C09-4329-A005-ABFF36C45E6E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebApp.md
ms.openlocfilehash: 64945cf503248fc0561dc894090c73d2d7151e4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733076"
---
# <span data-ttu-id="ecdfb-101">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ecdfb-101">Get-AzureRmWebApp</span></span>

## <span data-ttu-id="ecdfb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ecdfb-102">SYNOPSIS</span></span>
<span data-ttu-id="ecdfb-103">Получение веб-приложений Azure в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ecdfb-103">Gets Azure Web Apps in the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ecdfb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ecdfb-104">SYNTAX</span></span>

### <span data-ttu-id="ecdfb-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="ecdfb-105">S1</span></span>
```
Get-AzureRmWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ecdfb-106">S2</span><span class="sxs-lookup"><span data-stu-id="ecdfb-106">S2</span></span>
```
Get-AzureRmWebApp [-AppServicePlan] <ServerFarmWithRichSku> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ecdfb-107">Режима</span><span class="sxs-lookup"><span data-stu-id="ecdfb-107">S3</span></span>
```
Get-AzureRmWebApp [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ecdfb-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ecdfb-108">DESCRIPTION</span></span>
<span data-ttu-id="ecdfb-109">Командлет **Get-AzureRmWebApp** получает сведения о веб-приложении Azure.</span><span class="sxs-lookup"><span data-stu-id="ecdfb-109">The **Get-AzureRmWebApp** cmdlet gets information about an Azure Web App.</span></span>

## <span data-ttu-id="ecdfb-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ecdfb-110">EXAMPLES</span></span>

### <span data-ttu-id="ecdfb-111">Пример 1: получение веб-приложения из группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="ecdfb-111">Example 1: Get a Web App from a resource group</span></span>
```
PS C:\>Get-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -SlotName "Slot001"
```

<span data-ttu-id="ecdfb-112">Эта команда получает веб-приложение ContosoSite, которое принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="ecdfb-112">This command gets the Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="ecdfb-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ecdfb-113">PARAMETERS</span></span>

### <span data-ttu-id="ecdfb-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ecdfb-114">-AppServicePlan</span></span>
<span data-ttu-id="ecdfb-115">Объект плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="ecdfb-115">App Service Plan object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecdfb-116">-Location</span><span class="sxs-lookup"><span data-stu-id="ecdfb-116">-Location</span></span>
<span data-ttu-id="ecdfb-117">Поиска</span><span class="sxs-lookup"><span data-stu-id="ecdfb-117">Location</span></span>

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

### <span data-ttu-id="ecdfb-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ecdfb-118">-Name</span></span>
<span data-ttu-id="ecdfb-119">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="ecdfb-119">WebApp Name</span></span>

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

### <span data-ttu-id="ecdfb-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecdfb-120">-ResourceGroupName</span></span>
<span data-ttu-id="ecdfb-121">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="ecdfb-121">Resource Group Name</span></span>

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

### <span data-ttu-id="ecdfb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecdfb-122">-DefaultProfile</span></span>
<span data-ttu-id="ecdfb-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ecdfb-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ecdfb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecdfb-124">CommonParameters</span></span>
<span data-ttu-id="ecdfb-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ecdfb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecdfb-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecdfb-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecdfb-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ecdfb-127">INPUTS</span></span>

## <span data-ttu-id="ecdfb-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ecdfb-128">OUTPUTS</span></span>

## <span data-ttu-id="ecdfb-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="ecdfb-129">NOTES</span></span>

## <span data-ttu-id="ecdfb-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ecdfb-130">RELATED LINKS</span></span>

[<span data-ttu-id="ecdfb-131">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ecdfb-131">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="ecdfb-132">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ecdfb-132">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="ecdfb-133">Restarting-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ecdfb-133">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="ecdfb-134">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ecdfb-134">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="ecdfb-135">Остановить-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ecdfb-135">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


