---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 297071E5-FC06-4493-BCC2-37D4929E4025
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restart-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebApp.md
ms.openlocfilehash: faa3264dbf9fa65a2970f578c635868d185f2ef8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249244"
---
# <span data-ttu-id="52030-101">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="52030-101">Restart-AzWebApp</span></span>

## <span data-ttu-id="52030-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="52030-102">SYNOPSIS</span></span>
<span data-ttu-id="52030-103">Перезапускает веб-приложение Azure.</span><span class="sxs-lookup"><span data-stu-id="52030-103">Restarts an Azure Web App.</span></span>

## <span data-ttu-id="52030-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="52030-104">SYNTAX</span></span>

### <span data-ttu-id="52030-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="52030-105">S1</span></span>
```
Restart-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="52030-106">S2</span><span class="sxs-lookup"><span data-stu-id="52030-106">S2</span></span>
```
Restart-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52030-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="52030-107">DESCRIPTION</span></span>
<span data-ttu-id="52030-108">Командлет **restart-AzWebApp** останавливается, а затем запускает веб-приложение Azure.</span><span class="sxs-lookup"><span data-stu-id="52030-108">The **Restart-AzWebApp** cmdlet stops and then starts an Azure Web App.</span></span>
<span data-ttu-id="52030-109">Если веб-приложение находится в остановленном состоянии, используйте командлет Start-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="52030-109">If the Web App is in a stopped state, use the Start-AzWebApp cmdlet.</span></span>

## <span data-ttu-id="52030-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="52030-110">EXAMPLES</span></span>

### <span data-ttu-id="52030-111">Пример 1: перезагрузка веб-приложения</span><span class="sxs-lookup"><span data-stu-id="52030-111">Example 1: Restart a Web App</span></span>
```
PS C:\>Restart-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="52030-112">Эта команда останавливает веб-приложение Azure с именем ContosoSite, которое принадлежит группе ресурсов Default-Web-WestUS, а затем перезапускает ее.</span><span class="sxs-lookup"><span data-stu-id="52030-112">This command stops the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS and then restarts it.</span></span>

## <span data-ttu-id="52030-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="52030-113">PARAMETERS</span></span>

### <span data-ttu-id="52030-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52030-114">-DefaultProfile</span></span>
<span data-ttu-id="52030-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="52030-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52030-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="52030-116">-Name</span></span>
<span data-ttu-id="52030-117">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="52030-117">WebApp Name</span></span>

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

### <span data-ttu-id="52030-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52030-118">-ResourceGroupName</span></span>
<span data-ttu-id="52030-119">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="52030-119">Resource Group Name</span></span>

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

### <span data-ttu-id="52030-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="52030-120">-WebApp</span></span>
<span data-ttu-id="52030-121">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="52030-121">WebApp Object</span></span>

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

### <span data-ttu-id="52030-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52030-122">CommonParameters</span></span>
<span data-ttu-id="52030-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="52030-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52030-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52030-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52030-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="52030-125">INPUTS</span></span>

### <span data-ttu-id="52030-126">System. String</span><span class="sxs-lookup"><span data-stu-id="52030-126">System.String</span></span>

### <span data-ttu-id="52030-127">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="52030-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="52030-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="52030-128">OUTPUTS</span></span>

### <span data-ttu-id="52030-129">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="52030-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="52030-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="52030-130">NOTES</span></span>

## <span data-ttu-id="52030-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="52030-131">RELATED LINKS</span></span>

[<span data-ttu-id="52030-132">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="52030-132">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="52030-133">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="52030-133">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="52030-134">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="52030-134">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="52030-135">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="52030-135">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="52030-136">Остановить-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="52030-136">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)

