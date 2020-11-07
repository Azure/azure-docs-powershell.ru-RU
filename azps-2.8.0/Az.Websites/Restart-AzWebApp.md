---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 297071E5-FC06-4493-BCC2-37D4929E4025
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restart-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebApp.md
ms.openlocfilehash: 5b14c694ca61d5c63642012aa954b0e288551b83
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93907054"
---
# <span data-ttu-id="3f3dd-101">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3f3dd-101">Restart-AzWebApp</span></span>

## <span data-ttu-id="3f3dd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3f3dd-102">SYNOPSIS</span></span>
<span data-ttu-id="3f3dd-103">Перезапускает веб-приложение Azure.</span><span class="sxs-lookup"><span data-stu-id="3f3dd-103">Restarts an Azure Web App.</span></span>

## <span data-ttu-id="3f3dd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3f3dd-104">SYNTAX</span></span>

### <span data-ttu-id="3f3dd-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="3f3dd-105">S1</span></span>
```
Restart-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3f3dd-106">S2</span><span class="sxs-lookup"><span data-stu-id="3f3dd-106">S2</span></span>
```
Restart-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f3dd-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f3dd-107">DESCRIPTION</span></span>
<span data-ttu-id="3f3dd-108">Командлет **restart-AzWebApp** останавливается, а затем запускает веб-приложение Azure.</span><span class="sxs-lookup"><span data-stu-id="3f3dd-108">The **Restart-AzWebApp** cmdlet stops and then starts an Azure Web App.</span></span>
<span data-ttu-id="3f3dd-109">Если веб-приложение находится в остановленном состоянии, используйте командлет Start-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="3f3dd-109">If the Web App is in a stopped state, use the Start-AzWebApp cmdlet.</span></span>

## <span data-ttu-id="3f3dd-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3f3dd-110">EXAMPLES</span></span>

### <span data-ttu-id="3f3dd-111">Пример 1: перезагрузка веб-приложения</span><span class="sxs-lookup"><span data-stu-id="3f3dd-111">Example 1: Restart a Web App</span></span>
```
PS C:\>Restart-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="3f3dd-112">Эта команда останавливает веб-приложение Azure с именем ContosoSite, которое принадлежит группе ресурсов Default-Web-WestUS, а затем перезапускает ее.</span><span class="sxs-lookup"><span data-stu-id="3f3dd-112">This command stops the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS and then restarts it.</span></span>

## <span data-ttu-id="3f3dd-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3f3dd-113">PARAMETERS</span></span>

### <span data-ttu-id="3f3dd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f3dd-114">-DefaultProfile</span></span>
<span data-ttu-id="3f3dd-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3f3dd-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f3dd-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3f3dd-116">-Name</span></span>
<span data-ttu-id="3f3dd-117">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="3f3dd-117">WebApp Name</span></span>

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

### <span data-ttu-id="3f3dd-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f3dd-118">-ResourceGroupName</span></span>
<span data-ttu-id="3f3dd-119">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="3f3dd-119">Resource Group Name</span></span>

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

### <span data-ttu-id="3f3dd-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="3f3dd-120">-WebApp</span></span>
<span data-ttu-id="3f3dd-121">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="3f3dd-121">WebApp Object</span></span>

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

### <span data-ttu-id="3f3dd-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f3dd-122">CommonParameters</span></span>
<span data-ttu-id="3f3dd-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3f3dd-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f3dd-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f3dd-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f3dd-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3f3dd-125">INPUTS</span></span>

### <span data-ttu-id="3f3dd-126">System. String</span><span class="sxs-lookup"><span data-stu-id="3f3dd-126">System.String</span></span>

### <span data-ttu-id="3f3dd-127">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="3f3dd-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="3f3dd-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f3dd-128">OUTPUTS</span></span>

### <span data-ttu-id="3f3dd-129">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="3f3dd-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="3f3dd-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="3f3dd-130">NOTES</span></span>

## <span data-ttu-id="3f3dd-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3f3dd-131">RELATED LINKS</span></span>

[<span data-ttu-id="3f3dd-132">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3f3dd-132">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="3f3dd-133">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3f3dd-133">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="3f3dd-134">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3f3dd-134">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="3f3dd-135">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3f3dd-135">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="3f3dd-136">Остановить-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3f3dd-136">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


