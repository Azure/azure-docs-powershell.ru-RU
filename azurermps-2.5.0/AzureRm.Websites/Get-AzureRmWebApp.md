---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: A87ED954-9C09-4329-A005-ABFF36C45E6E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebapp
schema: 2.0.0
ms.openlocfilehash: eb1f96eaf85e6a5e7234e09c319b2e0c1117d456
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913256"
---
# <span data-ttu-id="0f064-101">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0f064-101">Get-AzureRmWebApp</span></span>

## <span data-ttu-id="0f064-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0f064-102">SYNOPSIS</span></span>
<span data-ttu-id="0f064-103">Получение веб-приложений Azure в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0f064-103">Gets Azure Web Apps in the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f064-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0f064-104">SYNTAX</span></span>

### <span data-ttu-id="0f064-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="0f064-105">S1</span></span>
```
Get-AzureRmWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0f064-106">S2</span><span class="sxs-lookup"><span data-stu-id="0f064-106">S2</span></span>
```
Get-AzureRmWebApp [-AppServicePlan] <AppServicePlan> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0f064-107">Режима</span><span class="sxs-lookup"><span data-stu-id="0f064-107">S3</span></span>
```
Get-AzureRmWebApp [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f064-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0f064-108">DESCRIPTION</span></span>
<span data-ttu-id="0f064-109">Командлет **Get-AzureRmWebApp** получает сведения о веб-приложении Azure.</span><span class="sxs-lookup"><span data-stu-id="0f064-109">The **Get-AzureRmWebApp** cmdlet gets information about an Azure Web App.</span></span>

## <span data-ttu-id="0f064-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0f064-110">EXAMPLES</span></span>

### <span data-ttu-id="0f064-111">Пример 1: получение веб-приложения из группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="0f064-111">Example 1: Get a Web App from a resource group</span></span>
```
PS C:\>Get-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="0f064-112">Эта команда получает веб-приложение ContosoSite, которое принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="0f064-112">This command gets the Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="0f064-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0f064-113">PARAMETERS</span></span>

### <span data-ttu-id="0f064-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0f064-114">-AppServicePlan</span></span>
<span data-ttu-id="0f064-115">Объект плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="0f064-115">App Service Plan object</span></span>

```yaml
Type: AppServicePlan
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f064-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f064-116">-DefaultProfile</span></span>
<span data-ttu-id="0f064-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0f064-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f064-118">-Location</span><span class="sxs-lookup"><span data-stu-id="0f064-118">-Location</span></span>
<span data-ttu-id="0f064-119">Поиска</span><span class="sxs-lookup"><span data-stu-id="0f064-119">Location</span></span>

```yaml
Type: String
Parameter Sets: S3
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f064-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0f064-120">-Name</span></span>
<span data-ttu-id="0f064-121">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="0f064-121">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f064-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f064-122">-ResourceGroupName</span></span>
<span data-ttu-id="0f064-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="0f064-123">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f064-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f064-124">CommonParameters</span></span>
<span data-ttu-id="0f064-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0f064-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f064-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f064-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f064-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0f064-127">INPUTS</span></span>

### <span data-ttu-id="0f064-128">System. String</span><span class="sxs-lookup"><span data-stu-id="0f064-128">System.String</span></span>

## <span data-ttu-id="0f064-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0f064-129">OUTPUTS</span></span>

### <span data-ttu-id="0f064-130">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="0f064-130">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="0f064-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="0f064-131">NOTES</span></span>

## <span data-ttu-id="0f064-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0f064-132">RELATED LINKS</span></span>

[<span data-ttu-id="0f064-133">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0f064-133">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="0f064-134">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0f064-134">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="0f064-135">Restarting-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0f064-135">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="0f064-136">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0f064-136">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="0f064-137">Остановить-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0f064-137">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


