---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 100A5980-31E2-41F9-84D4-2F5F0CB78B8A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlot.md
ms.openlocfilehash: 841cc1f8356d9b082dec55e689033c19343041d3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561971"
---
# <span data-ttu-id="9aee7-101">Get-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9aee7-101">Get-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="9aee7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9aee7-102">SYNOPSIS</span></span>
<span data-ttu-id="9aee7-103">Получает слот веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="9aee7-103">Gets an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9aee7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9aee7-104">SYNTAX</span></span>

### <span data-ttu-id="9aee7-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="9aee7-105">S1</span></span>
```
Get-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9aee7-106">S2</span><span class="sxs-lookup"><span data-stu-id="9aee7-106">S2</span></span>
```
Get-AzureRmWebAppSlot [[-Slot] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9aee7-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9aee7-107">DESCRIPTION</span></span>
<span data-ttu-id="9aee7-108">Командлет **Get-AzureRmWebAppSlot** получает сведения о слоте веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="9aee7-108">The **Get-AzureRmWebAppSlot** cmdlet gets information about an Azure Web App Slot.</span></span>

## <span data-ttu-id="9aee7-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9aee7-109">EXAMPLES</span></span>

### <span data-ttu-id="9aee7-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9aee7-110">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -Slot "Slot001"
```

<span data-ttu-id="9aee7-111">Эта команда получает слот с именем Slot001 из веб-приложения WebAppStandard, которое принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="9aee7-111">This command gets the slot named Slot001 from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="9aee7-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9aee7-112">PARAMETERS</span></span>

### <span data-ttu-id="9aee7-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9aee7-113">-Name</span></span>
<span data-ttu-id="9aee7-114">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="9aee7-114">WebApp Name</span></span>

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

### <span data-ttu-id="9aee7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9aee7-115">-ResourceGroupName</span></span>
<span data-ttu-id="9aee7-116">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="9aee7-116">Resource Group Name</span></span>

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

### <span data-ttu-id="9aee7-117">-Slot</span><span class="sxs-lookup"><span data-stu-id="9aee7-117">-Slot</span></span>
<span data-ttu-id="9aee7-118">Название гнезда WebApp</span><span class="sxs-lookup"><span data-stu-id="9aee7-118">WebApp Slot Name</span></span>

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

### <span data-ttu-id="9aee7-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="9aee7-119">-WebApp</span></span>
<span data-ttu-id="9aee7-120">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="9aee7-120">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9aee7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9aee7-121">-DefaultProfile</span></span>
<span data-ttu-id="9aee7-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9aee7-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9aee7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9aee7-123">CommonParameters</span></span>
<span data-ttu-id="9aee7-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9aee7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9aee7-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9aee7-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9aee7-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9aee7-126">INPUTS</span></span>

### <span data-ttu-id="9aee7-127">Семейств</span><span class="sxs-lookup"><span data-stu-id="9aee7-127">Site</span></span>
<span data-ttu-id="9aee7-128">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="9aee7-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="9aee7-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9aee7-129">OUTPUTS</span></span>

## <span data-ttu-id="9aee7-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="9aee7-130">NOTES</span></span>

## <span data-ttu-id="9aee7-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9aee7-131">RELATED LINKS</span></span>

[<span data-ttu-id="9aee7-132">New-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9aee7-132">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="9aee7-133">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9aee7-133">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="9aee7-134">Restarting-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9aee7-134">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="9aee7-135">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9aee7-135">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="9aee7-136">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9aee7-136">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="9aee7-137">Остановить-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9aee7-137">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="9aee7-138">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="9aee7-138">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
