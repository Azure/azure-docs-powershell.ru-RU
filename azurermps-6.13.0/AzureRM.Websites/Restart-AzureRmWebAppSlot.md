---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 645E74D2-640D-494F-9798-4375FE6A0AF2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restart-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restart-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restart-AzureRmWebAppSlot.md
ms.openlocfilehash: 2d1c4fe635e6d4bc509f82f1af376ee0f662217a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565289"
---
# <span data-ttu-id="69819-101">Restart-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="69819-101">Restart-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="69819-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="69819-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69819-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="69819-103">SYNTAX</span></span>

### <span data-ttu-id="69819-104">Состояний</span><span class="sxs-lookup"><span data-stu-id="69819-104">S1</span></span>
```
Restart-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69819-105">S2</span><span class="sxs-lookup"><span data-stu-id="69819-105">S2</span></span>
```
Restart-AzureRmWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69819-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="69819-106">DESCRIPTION</span></span>
<span data-ttu-id="69819-107">Командлет **restarting-AzureRmWebAppSlot** останавливается, а затем запускает слот веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="69819-107">The **Restart-AzureRmWebAppSlot** cmdlet stops and then starts an Azure Web App Slot.</span></span>
<span data-ttu-id="69819-108">Если ячейка веб-приложения находится в остановленном состоянии, используйте командлет Start-AzureRmWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="69819-108">If the Web App Slot is in a stopped state, use the Start-AzureRmWebAppSlot cmdlet.</span></span>

## <span data-ttu-id="69819-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="69819-109">EXAMPLES</span></span>

### <span data-ttu-id="69819-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="69819-110">Example 1</span></span>
```
PS C:\> Restart-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="69819-111">Эта команда перезапускает слот Slot001 для веб-приложения ContosoWebApp, связанного с группой ресурсов по умолчанию — Web-WestUS</span><span class="sxs-lookup"><span data-stu-id="69819-111">This command restarts the slot Slot001 for the web app ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="69819-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="69819-112">PARAMETERS</span></span>

### <span data-ttu-id="69819-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69819-113">-DefaultProfile</span></span>
<span data-ttu-id="69819-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="69819-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69819-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="69819-115">-Name</span></span>
<span data-ttu-id="69819-116">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="69819-116">WebApp Name</span></span>

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

### <span data-ttu-id="69819-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69819-117">-ResourceGroupName</span></span>
<span data-ttu-id="69819-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="69819-118">Resource Group Name</span></span>

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

### <span data-ttu-id="69819-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="69819-119">-Slot</span></span>
<span data-ttu-id="69819-120">Название гнезда WebApp</span><span class="sxs-lookup"><span data-stu-id="69819-120">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69819-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="69819-121">-WebApp</span></span>
<span data-ttu-id="69819-122">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="69819-122">WebApp Object</span></span>

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

### <span data-ttu-id="69819-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69819-123">CommonParameters</span></span>
<span data-ttu-id="69819-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="69819-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69819-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69819-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69819-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="69819-126">INPUTS</span></span>

### <span data-ttu-id="69819-127">System. String</span><span class="sxs-lookup"><span data-stu-id="69819-127">System.String</span></span>

### <span data-ttu-id="69819-128">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="69819-128">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="69819-129">Параметры: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="69819-129">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="69819-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="69819-130">OUTPUTS</span></span>

### <span data-ttu-id="69819-131">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="69819-131">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="69819-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="69819-132">NOTES</span></span>

## <span data-ttu-id="69819-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="69819-133">RELATED LINKS</span></span>

[<span data-ttu-id="69819-134">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="69819-134">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="69819-135">New-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="69819-135">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="69819-136">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="69819-136">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="69819-137">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="69819-137">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="69819-138">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="69819-138">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="69819-139">Остановить-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="69819-139">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="69819-140">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="69819-140">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
