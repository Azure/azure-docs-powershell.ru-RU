---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: AD76C752-2070-449D-BF4F-B4260B05AB02
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/update-azurermsiterecoveryserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServer.md
ms.openlocfilehash: ce38334d3ae37864d53830970d895e29755f6687
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557115"
---
# <span data-ttu-id="01376-101">Update-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="01376-101">Update-AzureRmSiteRecoveryServer</span></span>

## <span data-ttu-id="01376-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="01376-102">SYNOPSIS</span></span>
<span data-ttu-id="01376-103">Обновляет сервер восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="01376-103">Refreshes a Site Recovery server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01376-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="01376-104">SYNTAX</span></span>

```
Update-AzureRmSiteRecoveryServer -Server <ASRServer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="01376-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="01376-105">DESCRIPTION</span></span>
<span data-ttu-id="01376-106">Командлет **Update-AzureRmSiteRecoveryServer** обновляет сервер Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="01376-106">The **Update-AzureRmSiteRecoveryServer** cmdlet refreshes an Azure Site Recovery server.</span></span>

## <span data-ttu-id="01376-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="01376-107">EXAMPLES</span></span>

## <span data-ttu-id="01376-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="01376-108">PARAMETERS</span></span>

### <span data-ttu-id="01376-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01376-109">-DefaultProfile</span></span>
<span data-ttu-id="01376-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="01376-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01376-111">-Сервер</span><span class="sxs-lookup"><span data-stu-id="01376-111">-Server</span></span>
<span data-ttu-id="01376-112">Указывает сервер восстановления сайта, который обновляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="01376-112">Specifies the Site Recovery server that this cmdlet updates.</span></span>

```yaml
Type: ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01376-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01376-113">CommonParameters</span></span>
<span data-ttu-id="01376-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="01376-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01376-115">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01376-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01376-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="01376-116">INPUTS</span></span>

### <span data-ttu-id="01376-117">ASRServer</span><span class="sxs-lookup"><span data-stu-id="01376-117">ASRServer</span></span>
<span data-ttu-id="01376-118">Параметр Server принимает значение типа "ASRServer" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="01376-118">Parameter 'Server' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="01376-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="01376-119">OUTPUTS</span></span>

## <span data-ttu-id="01376-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="01376-120">NOTES</span></span>

## <span data-ttu-id="01376-121">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="01376-121">RELATED LINKS</span></span>

[<span data-ttu-id="01376-122">Get-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="01376-122">Get-AzureRmSiteRecoveryServer</span></span>](./Get-AzureRmSiteRecoveryServer.md)

[<span data-ttu-id="01376-123">Remove-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="01376-123">Remove-AzureRmSiteRecoveryServer</span></span>](./Remove-AzureRmSiteRecoveryServer.md)
