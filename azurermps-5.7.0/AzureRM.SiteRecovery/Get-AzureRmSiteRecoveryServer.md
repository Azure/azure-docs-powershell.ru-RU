---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: CFB7CF64-1415-44B3-932B-2A5613666D3E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryServer.md
ms.openlocfilehash: feba4e66483aba9e77817aa2b473d0d22ae7d882
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733979"
---
# <span data-ttu-id="84918-101">Get-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="84918-101">Get-AzureRmSiteRecoveryServer</span></span>

## <span data-ttu-id="84918-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="84918-102">SYNOPSIS</span></span>
<span data-ttu-id="84918-103">Возвращает сведения о серверах восстановления сайта, зарегистрированных в текущем хранилище.</span><span class="sxs-lookup"><span data-stu-id="84918-103">Gets information about Site Recovery servers registered to the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84918-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="84918-104">SYNTAX</span></span>

### <span data-ttu-id="84918-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="84918-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryServer [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84918-106">ByName</span><span class="sxs-lookup"><span data-stu-id="84918-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryServer -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84918-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="84918-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryServer -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="84918-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="84918-108">DESCRIPTION</span></span>
<span data-ttu-id="84918-109">Командлет **Get-AzureRmSiteRecoveryServer** получает сведения о серверах Azure Site Recovery, зарегистрированных в текущем хранилище сайта для восстановления.</span><span class="sxs-lookup"><span data-stu-id="84918-109">The **Get-AzureRmSiteRecoveryServer** cmdlet gets information about Azure Site Recovery servers registered to the current Site Recovery vault.</span></span>

## <span data-ttu-id="84918-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="84918-110">EXAMPLES</span></span>

## <span data-ttu-id="84918-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="84918-111">PARAMETERS</span></span>

### <span data-ttu-id="84918-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84918-112">-DefaultProfile</span></span>
<span data-ttu-id="84918-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="84918-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84918-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="84918-114">-FriendlyName</span></span>
<span data-ttu-id="84918-115">Указывает понятное имя сервера.</span><span class="sxs-lookup"><span data-stu-id="84918-115">Specifies the friendly name of the server.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84918-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="84918-116">-Name</span></span>
<span data-ttu-id="84918-117">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="84918-117">Specifies the name of the server.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84918-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84918-118">CommonParameters</span></span>
<span data-ttu-id="84918-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="84918-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84918-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84918-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84918-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="84918-121">INPUTS</span></span>

### <span data-ttu-id="84918-122">Ничего</span><span class="sxs-lookup"><span data-stu-id="84918-122">None</span></span>
<span data-ttu-id="84918-123">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="84918-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="84918-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="84918-124">OUTPUTS</span></span>

### <span data-ttu-id="84918-125">System. Collections. Generic. IEnumerable 1 [Microsoft. Azure. Commands. SiteRecovery. ASRServer]</span><span class="sxs-lookup"><span data-stu-id="84918-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRServer]</span></span>

## <span data-ttu-id="84918-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="84918-126">NOTES</span></span>

## <span data-ttu-id="84918-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="84918-127">RELATED LINKS</span></span>

[<span data-ttu-id="84918-128">Remove-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="84918-128">Remove-AzureRmSiteRecoveryServer</span></span>](./Remove-AzureRmSiteRecoveryServer.md)
