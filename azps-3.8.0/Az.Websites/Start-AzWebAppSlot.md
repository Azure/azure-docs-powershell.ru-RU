---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 0FDDDEE1-CEAD-46DA-A7EB-EE477ED59749
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/start-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebAppSlot.md
ms.openlocfilehash: 4425c344fb0c9e0e3441c172915be11002ee8b1b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94072587"
---
# <span data-ttu-id="1b6f4-101">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="1b6f4-101">Start-AzWebAppSlot</span></span>

## <span data-ttu-id="1b6f4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1b6f4-102">SYNOPSIS</span></span>
<span data-ttu-id="1b6f4-103">Запускает слот веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="1b6f4-103">Starts an Azure Web App slot.</span></span>

## <span data-ttu-id="1b6f4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1b6f4-104">SYNTAX</span></span>

### <span data-ttu-id="1b6f4-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="1b6f4-105">S1</span></span>
```
Start-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b6f4-106">S2</span><span class="sxs-lookup"><span data-stu-id="1b6f4-106">S2</span></span>
```
Start-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b6f4-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1b6f4-107">DESCRIPTION</span></span>
<span data-ttu-id="1b6f4-108">Командлет **Start-AzWebAppSlot** запускает слот веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="1b6f4-108">The **Start-AzWebAppSlot** cmdlet starts an Azure Web App Slot.</span></span>

## <span data-ttu-id="1b6f4-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1b6f4-109">EXAMPLES</span></span>

### <span data-ttu-id="1b6f4-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1b6f4-110">Example 1</span></span>
```
PS C:\>Start-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="1b6f4-111">Эта команда запускает ячейку с именем Slot001, относящуюся к веб-приложению ContosoWebApp, которое принадлежит группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="1b6f4-111">This command starts the Slot named Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="1b6f4-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1b6f4-112">PARAMETERS</span></span>

### <span data-ttu-id="1b6f4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b6f4-113">-DefaultProfile</span></span>
<span data-ttu-id="1b6f4-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1b6f4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b6f4-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1b6f4-115">-Name</span></span>
<span data-ttu-id="1b6f4-116">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="1b6f4-116">WebApp Name</span></span>

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

### <span data-ttu-id="1b6f4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b6f4-117">-ResourceGroupName</span></span>
<span data-ttu-id="1b6f4-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="1b6f4-118">Resource Group Name</span></span>

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

### <span data-ttu-id="1b6f4-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="1b6f4-119">-Slot</span></span>
<span data-ttu-id="1b6f4-120">Название гнезда WebApp</span><span class="sxs-lookup"><span data-stu-id="1b6f4-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="1b6f4-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="1b6f4-121">-WebApp</span></span>
<span data-ttu-id="1b6f4-122">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="1b6f4-122">WebApp Object</span></span>

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

### <span data-ttu-id="1b6f4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b6f4-123">CommonParameters</span></span>
<span data-ttu-id="1b6f4-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1b6f4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b6f4-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b6f4-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b6f4-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1b6f4-126">INPUTS</span></span>

### <span data-ttu-id="1b6f4-127">System. String</span><span class="sxs-lookup"><span data-stu-id="1b6f4-127">System.String</span></span>

### <span data-ttu-id="1b6f4-128">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="1b6f4-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="1b6f4-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1b6f4-129">OUTPUTS</span></span>

### <span data-ttu-id="1b6f4-130">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="1b6f4-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="1b6f4-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="1b6f4-131">NOTES</span></span>

## <span data-ttu-id="1b6f4-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1b6f4-132">RELATED LINKS</span></span>

[<span data-ttu-id="1b6f4-133">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="1b6f4-133">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="1b6f4-134">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="1b6f4-134">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="1b6f4-135">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="1b6f4-135">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="1b6f4-136">Restarting-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="1b6f4-136">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="1b6f4-137">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="1b6f4-137">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="1b6f4-138">Остановить-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="1b6f4-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="1b6f4-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1b6f4-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
