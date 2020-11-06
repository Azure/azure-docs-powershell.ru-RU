---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 0FDDDEE1-CEAD-46DA-A7EB-EE477ED59749
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/start-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Start-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Start-AzureRmWebAppSlot.md
ms.openlocfilehash: 089711bacd6401b4c44683a159e43a92a56106d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558107"
---
# <span data-ttu-id="2c3ce-101">Start-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2c3ce-101">Start-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="2c3ce-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2c3ce-102">SYNOPSIS</span></span>
<span data-ttu-id="2c3ce-103">Запускает слот веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="2c3ce-103">Starts an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c3ce-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2c3ce-104">SYNTAX</span></span>

### <span data-ttu-id="2c3ce-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="2c3ce-105">S1</span></span>
```
Start-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c3ce-106">S2</span><span class="sxs-lookup"><span data-stu-id="2c3ce-106">S2</span></span>
```
Start-AzureRmWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c3ce-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c3ce-107">DESCRIPTION</span></span>
<span data-ttu-id="2c3ce-108">Командлет **Start-AzureRmWebAppSlot** запускает слот веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="2c3ce-108">The **Start-AzureRmWebAppSlot** cmdlet starts an Azure Web App Slot.</span></span>

## <span data-ttu-id="2c3ce-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2c3ce-109">EXAMPLES</span></span>

### <span data-ttu-id="2c3ce-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2c3ce-110">Example 1</span></span>
```
PS C:\>Start-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="2c3ce-111">Эта команда запускает ячейку с именем Slot001, относящуюся к веб-приложению ContosoWebApp, которое принадлежит группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="2c3ce-111">This command starts the Slot named Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="2c3ce-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2c3ce-112">PARAMETERS</span></span>

### <span data-ttu-id="2c3ce-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c3ce-113">-DefaultProfile</span></span>
<span data-ttu-id="2c3ce-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2c3ce-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c3ce-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2c3ce-115">-Name</span></span>
<span data-ttu-id="2c3ce-116">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="2c3ce-116">WebApp Name</span></span>

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

### <span data-ttu-id="2c3ce-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c3ce-117">-ResourceGroupName</span></span>
<span data-ttu-id="2c3ce-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="2c3ce-118">Resource Group Name</span></span>

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

### <span data-ttu-id="2c3ce-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="2c3ce-119">-Slot</span></span>
<span data-ttu-id="2c3ce-120">Название гнезда WebApp</span><span class="sxs-lookup"><span data-stu-id="2c3ce-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="2c3ce-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="2c3ce-121">-WebApp</span></span>
<span data-ttu-id="2c3ce-122">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="2c3ce-122">WebApp Object</span></span>

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

### <span data-ttu-id="2c3ce-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c3ce-123">CommonParameters</span></span>
<span data-ttu-id="2c3ce-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2c3ce-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c3ce-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c3ce-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c3ce-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2c3ce-126">INPUTS</span></span>

### <span data-ttu-id="2c3ce-127">System. String</span><span class="sxs-lookup"><span data-stu-id="2c3ce-127">System.String</span></span>

### <span data-ttu-id="2c3ce-128">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="2c3ce-128">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="2c3ce-129">Параметры: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2c3ce-129">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="2c3ce-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c3ce-130">OUTPUTS</span></span>

### <span data-ttu-id="2c3ce-131">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="2c3ce-131">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="2c3ce-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="2c3ce-132">NOTES</span></span>

## <span data-ttu-id="2c3ce-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2c3ce-133">RELATED LINKS</span></span>

[<span data-ttu-id="2c3ce-134">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2c3ce-134">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="2c3ce-135">New-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2c3ce-135">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="2c3ce-136">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2c3ce-136">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="2c3ce-137">Restarting-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2c3ce-137">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="2c3ce-138">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2c3ce-138">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="2c3ce-139">Остановить-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2c3ce-139">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="2c3ce-140">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="2c3ce-140">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
