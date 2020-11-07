---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: A87ED954-9C09-4329-A005-ABFF36C45E6E
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebApp.md
ms.openlocfilehash: f86e0f18c7d793b5876a48c39b56b11c14b17546
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910625"
---
# <span data-ttu-id="e636c-101">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e636c-101">Get-AzWebApp</span></span>

## <span data-ttu-id="e636c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e636c-102">SYNOPSIS</span></span>
<span data-ttu-id="e636c-103">Получение веб-приложений Azure в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e636c-103">Gets Azure Web Apps in the specified resource group.</span></span>

## <span data-ttu-id="e636c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e636c-104">SYNTAX</span></span>

### <span data-ttu-id="e636c-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="e636c-105">S1</span></span>
```
Get-AzWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e636c-106">S2</span><span class="sxs-lookup"><span data-stu-id="e636c-106">S2</span></span>
```
Get-AzWebApp [-AppServicePlan] <AppServicePlan> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e636c-107">Режима</span><span class="sxs-lookup"><span data-stu-id="e636c-107">S3</span></span>
```
Get-AzWebApp [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e636c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e636c-108">DESCRIPTION</span></span>
<span data-ttu-id="e636c-109">Командлет **Get-AzWebApp** получает сведения о веб-приложении Azure.</span><span class="sxs-lookup"><span data-stu-id="e636c-109">The **Get-AzWebApp** cmdlet gets information about an Azure Web App.</span></span>

## <span data-ttu-id="e636c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e636c-110">EXAMPLES</span></span>

### <span data-ttu-id="e636c-111">Пример 1: получение веб-приложения из группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="e636c-111">Example 1: Get a Web App from a resource group</span></span>
```
PS C:\>Get-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="e636c-112">Эта команда получает веб-приложение ContosoSite, которое принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="e636c-112">This command gets the Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="e636c-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e636c-113">PARAMETERS</span></span>

### <span data-ttu-id="e636c-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="e636c-114">-AppServicePlan</span></span>
<span data-ttu-id="e636c-115">Объект плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="e636c-115">App Service Plan object</span></span>

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

### <span data-ttu-id="e636c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e636c-116">-DefaultProfile</span></span>
<span data-ttu-id="e636c-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e636c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e636c-118">-Location</span><span class="sxs-lookup"><span data-stu-id="e636c-118">-Location</span></span>
<span data-ttu-id="e636c-119">Поиска</span><span class="sxs-lookup"><span data-stu-id="e636c-119">Location</span></span>

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

### <span data-ttu-id="e636c-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e636c-120">-Name</span></span>
<span data-ttu-id="e636c-121">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="e636c-121">WebApp Name</span></span>

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

### <span data-ttu-id="e636c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e636c-122">-ResourceGroupName</span></span>
<span data-ttu-id="e636c-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="e636c-123">Resource Group Name</span></span>

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

### <span data-ttu-id="e636c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e636c-124">CommonParameters</span></span>
<span data-ttu-id="e636c-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e636c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e636c-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e636c-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e636c-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e636c-127">INPUTS</span></span>

### <span data-ttu-id="e636c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="e636c-128">System.String</span></span>

## <span data-ttu-id="e636c-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e636c-129">OUTPUTS</span></span>

### <span data-ttu-id="e636c-130">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="e636c-130">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="e636c-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="e636c-131">NOTES</span></span>

## <span data-ttu-id="e636c-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e636c-132">RELATED LINKS</span></span>

[<span data-ttu-id="e636c-133">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e636c-133">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="e636c-134">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e636c-134">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="e636c-135">Restarting-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e636c-135">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="e636c-136">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e636c-136">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="e636c-137">Остановить-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e636c-137">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


