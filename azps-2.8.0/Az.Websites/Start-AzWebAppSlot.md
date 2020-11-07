---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 0FDDDEE1-CEAD-46DA-A7EB-EE477ED59749
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/start-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebAppSlot.md
ms.openlocfilehash: 0535eee5dcdc3d0e78f95951fddcca9d7b8fff3b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93907841"
---
# <span data-ttu-id="b2e02-101">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b2e02-101">Start-AzWebAppSlot</span></span>

## <span data-ttu-id="b2e02-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b2e02-102">SYNOPSIS</span></span>
<span data-ttu-id="b2e02-103">Запускает слот веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="b2e02-103">Starts an Azure Web App slot.</span></span>

## <span data-ttu-id="b2e02-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b2e02-104">SYNTAX</span></span>

### <span data-ttu-id="b2e02-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="b2e02-105">S1</span></span>
```
Start-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2e02-106">S2</span><span class="sxs-lookup"><span data-stu-id="b2e02-106">S2</span></span>
```
Start-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2e02-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b2e02-107">DESCRIPTION</span></span>
<span data-ttu-id="b2e02-108">Командлет **Start-AzWebAppSlot** запускает слот веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="b2e02-108">The **Start-AzWebAppSlot** cmdlet starts an Azure Web App Slot.</span></span>

## <span data-ttu-id="b2e02-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b2e02-109">EXAMPLES</span></span>

### <span data-ttu-id="b2e02-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b2e02-110">Example 1</span></span>
```
PS C:\>Start-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="b2e02-111">Эта команда запускает ячейку с именем Slot001, относящуюся к веб-приложению ContosoWebApp, которое принадлежит группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="b2e02-111">This command starts the Slot named Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="b2e02-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b2e02-112">PARAMETERS</span></span>

### <span data-ttu-id="b2e02-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2e02-113">-DefaultProfile</span></span>
<span data-ttu-id="b2e02-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b2e02-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2e02-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b2e02-115">-Name</span></span>
<span data-ttu-id="b2e02-116">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="b2e02-116">WebApp Name</span></span>

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

### <span data-ttu-id="b2e02-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2e02-117">-ResourceGroupName</span></span>
<span data-ttu-id="b2e02-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="b2e02-118">Resource Group Name</span></span>

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

### <span data-ttu-id="b2e02-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="b2e02-119">-Slot</span></span>
<span data-ttu-id="b2e02-120">Название гнезда WebApp</span><span class="sxs-lookup"><span data-stu-id="b2e02-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="b2e02-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="b2e02-121">-WebApp</span></span>
<span data-ttu-id="b2e02-122">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="b2e02-122">WebApp Object</span></span>

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

### <span data-ttu-id="b2e02-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2e02-123">CommonParameters</span></span>
<span data-ttu-id="b2e02-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b2e02-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2e02-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2e02-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2e02-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b2e02-126">INPUTS</span></span>

### <span data-ttu-id="b2e02-127">System. String</span><span class="sxs-lookup"><span data-stu-id="b2e02-127">System.String</span></span>

### <span data-ttu-id="b2e02-128">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="b2e02-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="b2e02-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b2e02-129">OUTPUTS</span></span>

### <span data-ttu-id="b2e02-130">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="b2e02-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="b2e02-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="b2e02-131">NOTES</span></span>

## <span data-ttu-id="b2e02-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b2e02-132">RELATED LINKS</span></span>

[<span data-ttu-id="b2e02-133">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b2e02-133">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="b2e02-134">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b2e02-134">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="b2e02-135">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b2e02-135">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="b2e02-136">Restarting-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b2e02-136">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="b2e02-137">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b2e02-137">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="b2e02-138">Остановить-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="b2e02-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="b2e02-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b2e02-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
