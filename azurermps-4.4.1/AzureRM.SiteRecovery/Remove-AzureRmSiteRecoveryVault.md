---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 63E9894A-3AC5-4397-9B21-D0A72EBA5C4B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryVault.md
ms.openlocfilehash: e5d85c6cdc30ff00d2a35bba6d1a79119cbaddd2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567048"
---
# <span data-ttu-id="ee2c0-101">Remove-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="ee2c0-101">Remove-AzureRmSiteRecoveryVault</span></span>

## <span data-ttu-id="ee2c0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ee2c0-102">SYNOPSIS</span></span>
<span data-ttu-id="ee2c0-103">Удаляет хранилище для восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="ee2c0-103">Removes a Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee2c0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ee2c0-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryVault -Vault <ASRVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ee2c0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ee2c0-105">DESCRIPTION</span></span>
<span data-ttu-id="ee2c0-106">Командлет **Remove-AzureRmSiteRecoveryVault** удаляет хранилище Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="ee2c0-106">The **Remove-AzureRmSiteRecoveryVault** cmdlet deletes an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="ee2c0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ee2c0-107">EXAMPLES</span></span>

## <span data-ttu-id="ee2c0-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ee2c0-108">PARAMETERS</span></span>

### <span data-ttu-id="ee2c0-109">-Хранилище</span><span class="sxs-lookup"><span data-stu-id="ee2c0-109">-Vault</span></span>
<span data-ttu-id="ee2c0-110">Указывает объект хранилища для восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="ee2c0-110">Specifies the Site Recovery vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ee2c0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee2c0-111">-DefaultProfile</span></span>
<span data-ttu-id="ee2c0-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ee2c0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee2c0-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee2c0-113">CommonParameters</span></span>
<span data-ttu-id="ee2c0-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ee2c0-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee2c0-115">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee2c0-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee2c0-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ee2c0-116">INPUTS</span></span>

### <span data-ttu-id="ee2c0-117">ASRVault</span><span class="sxs-lookup"><span data-stu-id="ee2c0-117">ASRVault</span></span>
<span data-ttu-id="ee2c0-118">Параметр "хранилище" принимает значение типа "ASRVault" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="ee2c0-118">Parameter 'Vault' accepts value of type 'ASRVault' from the pipeline</span></span>

## <span data-ttu-id="ee2c0-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ee2c0-119">OUTPUTS</span></span>

## <span data-ttu-id="ee2c0-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="ee2c0-120">NOTES</span></span>

## <span data-ttu-id="ee2c0-121">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ee2c0-121">RELATED LINKS</span></span>

[<span data-ttu-id="ee2c0-122">Get-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="ee2c0-122">Get-AzureRmSiteRecoveryVault</span></span>](./Get-AzureRmSiteRecoveryVault.md)

[<span data-ttu-id="ee2c0-123">New-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="ee2c0-123">New-AzureRmSiteRecoveryVault</span></span>](./New-AzureRmSiteRecoveryVault.md)
