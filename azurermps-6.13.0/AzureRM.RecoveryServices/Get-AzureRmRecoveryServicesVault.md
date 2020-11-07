---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/get-azurermrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: 0812fc8aa5673f6475fb822137cffff025003d32
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734916"
---
# <span data-ttu-id="e2560-101">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="e2560-101">Get-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="e2560-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e2560-102">SYNOPSIS</span></span>
<span data-ttu-id="e2560-103">Получает список хранилищ служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="e2560-103">Gets a list of Recovery Services vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2560-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e2560-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesVault [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2560-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2560-105">DESCRIPTION</span></span>
<span data-ttu-id="e2560-106">Командлет **Get-AzureRmRecoveryServicesVault** получает список хранилищ служб восстановления в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="e2560-106">The **Get-AzureRmRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="e2560-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e2560-107">EXAMPLES</span></span>

### <span data-ttu-id="e2560-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e2560-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesVault
```

<span data-ttu-id="e2560-109">Получение списка хранилищ в выбранной подписке.</span><span class="sxs-lookup"><span data-stu-id="e2560-109">Get the list of vault in selected subscription.</span></span>

### <span data-ttu-id="e2560-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e2560-110">Example 2</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

<span data-ttu-id="e2560-111">Получение списка хранилищ в группе ресурсов в выбранной подписке.</span><span class="sxs-lookup"><span data-stu-id="e2560-111">Get the list of vault in resource group in selected subscription.</span></span>

### <span data-ttu-id="e2560-112">Пример 3</span><span class="sxs-lookup"><span data-stu-id="e2560-112">Example 3</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
```

<span data-ttu-id="e2560-113">Получение хранилища в группе ресурсов с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="e2560-113">Get the vault in resource group with given name.</span></span>

## <span data-ttu-id="e2560-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e2560-114">PARAMETERS</span></span>

### <span data-ttu-id="e2560-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e2560-115">-Name</span></span>
<span data-ttu-id="e2560-116">Указывает имя хранилища для запроса.</span><span class="sxs-lookup"><span data-stu-id="e2560-116">Specifies the name of the vault to query for.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2560-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2560-117">-ResourceGroupName</span></span>
<span data-ttu-id="e2560-118">Указывает имя группы ресурсов Azure, в которой нужно создать или из которой нужно получить указанный объект служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="e2560-118">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2560-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2560-119">-DefaultProfile</span></span>
<span data-ttu-id="e2560-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e2560-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2560-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2560-121">CommonParameters</span></span>
<span data-ttu-id="e2560-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e2560-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2560-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2560-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2560-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e2560-124">INPUTS</span></span>

### <span data-ttu-id="e2560-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="e2560-125">None</span></span>

## <span data-ttu-id="e2560-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2560-126">OUTPUTS</span></span>

### <span data-ttu-id="e2560-127">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="e2560-127">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="e2560-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="e2560-128">NOTES</span></span>

## <span data-ttu-id="e2560-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e2560-129">RELATED LINKS</span></span>

[<span data-ttu-id="e2560-130">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="e2560-130">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="e2560-131">New-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="e2560-131">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="e2560-132">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="e2560-132">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


