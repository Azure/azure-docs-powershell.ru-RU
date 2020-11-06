---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 100A5980-31E2-41F9-84D4-2F5F0CB78B8A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlot.md
ms.openlocfilehash: f7be5b7877362484d0f3dfe4d19b8afc669e917c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556444"
---
# <span data-ttu-id="8f2ad-101">Get-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8f2ad-101">Get-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="8f2ad-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8f2ad-102">SYNOPSIS</span></span>
<span data-ttu-id="8f2ad-103">Получает слот веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="8f2ad-103">Gets an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f2ad-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8f2ad-104">SYNTAX</span></span>

### <span data-ttu-id="8f2ad-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="8f2ad-105">S1</span></span>
```
Get-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f2ad-106">S2</span><span class="sxs-lookup"><span data-stu-id="8f2ad-106">S2</span></span>
```
Get-AzureRmWebAppSlot [[-Slot] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8f2ad-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f2ad-107">DESCRIPTION</span></span>
<span data-ttu-id="8f2ad-108">Командлет **Get-AzureRmWebAppSlot** получает сведения о слоте веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="8f2ad-108">The **Get-AzureRmWebAppSlot** cmdlet gets information about an Azure Web App Slot.</span></span>

## <span data-ttu-id="8f2ad-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8f2ad-109">EXAMPLES</span></span>

### <span data-ttu-id="8f2ad-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8f2ad-110">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -Slot "Slot001"
```

<span data-ttu-id="8f2ad-111">Эта команда получает слот с именем Slot001 из веб-приложения WebAppStandard, которое принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="8f2ad-111">This command gets the slot named Slot001 from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="8f2ad-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8f2ad-112">PARAMETERS</span></span>

### <span data-ttu-id="8f2ad-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f2ad-113">-DefaultProfile</span></span>
<span data-ttu-id="8f2ad-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8f2ad-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f2ad-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8f2ad-115">-Name</span></span>
<span data-ttu-id="8f2ad-116">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="8f2ad-116">WebApp Name</span></span>

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

### <span data-ttu-id="8f2ad-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f2ad-117">-ResourceGroupName</span></span>
<span data-ttu-id="8f2ad-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="8f2ad-118">Resource Group Name</span></span>

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

### <span data-ttu-id="8f2ad-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="8f2ad-119">-Slot</span></span>
<span data-ttu-id="8f2ad-120">Название гнезда WebApp</span><span class="sxs-lookup"><span data-stu-id="8f2ad-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="8f2ad-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="8f2ad-121">-WebApp</span></span>
<span data-ttu-id="8f2ad-122">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="8f2ad-122">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f2ad-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f2ad-123">CommonParameters</span></span>
<span data-ttu-id="8f2ad-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8f2ad-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f2ad-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f2ad-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f2ad-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8f2ad-126">INPUTS</span></span>

### <span data-ttu-id="8f2ad-127">System. String</span><span class="sxs-lookup"><span data-stu-id="8f2ad-127">System.String</span></span>

### <span data-ttu-id="8f2ad-128">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="8f2ad-128">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="8f2ad-129">Параметры: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8f2ad-129">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="8f2ad-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f2ad-130">OUTPUTS</span></span>

### <span data-ttu-id="8f2ad-131">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="8f2ad-131">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="8f2ad-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="8f2ad-132">NOTES</span></span>

## <span data-ttu-id="8f2ad-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8f2ad-133">RELATED LINKS</span></span>

[<span data-ttu-id="8f2ad-134">New-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8f2ad-134">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="8f2ad-135">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8f2ad-135">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="8f2ad-136">Restarting-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8f2ad-136">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="8f2ad-137">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8f2ad-137">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="8f2ad-138">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8f2ad-138">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="8f2ad-139">Остановить-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8f2ad-139">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="8f2ad-140">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="8f2ad-140">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
