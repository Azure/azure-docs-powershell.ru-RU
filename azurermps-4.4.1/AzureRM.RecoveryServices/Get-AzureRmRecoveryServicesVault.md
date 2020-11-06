---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: bd9b47b54cb609a06da10488007f55d91d157b90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567532"
---
# <span data-ttu-id="4c826-101">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="4c826-101">Get-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="4c826-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4c826-102">SYNOPSIS</span></span>
<span data-ttu-id="4c826-103">Получает список хранилищ служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="4c826-103">Gets a list of Recovery Services vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c826-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4c826-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesVault [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c826-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4c826-105">DESCRIPTION</span></span>
<span data-ttu-id="4c826-106">Командлет **Get-AzureRmRecoveryServicesVault** получает список хранилищ служб восстановления в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="4c826-106">The **Get-AzureRmRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="4c826-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4c826-107">EXAMPLES</span></span>

## <span data-ttu-id="4c826-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4c826-108">PARAMETERS</span></span>

### <span data-ttu-id="4c826-109">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4c826-109">-Name</span></span>
<span data-ttu-id="4c826-110">Указывает имя хранилища для запроса.</span><span class="sxs-lookup"><span data-stu-id="4c826-110">Specifies the name of the vault to query for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c826-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c826-111">-ResourceGroupName</span></span>
<span data-ttu-id="4c826-112">Указывает имя группы ресурсов Azure, в которой нужно создать или из которой нужно получить указанный объект служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="4c826-112">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c826-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c826-113">-DefaultProfile</span></span>
<span data-ttu-id="4c826-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4c826-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c826-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c826-115">CommonParameters</span></span>
<span data-ttu-id="4c826-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4c826-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c826-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c826-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c826-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4c826-118">INPUTS</span></span>

## <span data-ttu-id="4c826-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4c826-119">OUTPUTS</span></span>

### <span data-ttu-id="4c826-120">System. Collections. Generic. List ' 1 [Microsoft. Azure. RecoveryServices. ARSVault]</span><span class="sxs-lookup"><span data-stu-id="4c826-120">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.RecoveryServices.ARSVault]</span></span>

## <span data-ttu-id="4c826-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="4c826-121">NOTES</span></span>

## <span data-ttu-id="4c826-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4c826-122">RELATED LINKS</span></span>

[<span data-ttu-id="4c826-123">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="4c826-123">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="4c826-124">New-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="4c826-124">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="4c826-125">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="4c826-125">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


