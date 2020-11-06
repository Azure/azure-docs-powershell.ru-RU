---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/get-azurermrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: bbc059751ee4713b59f6b915efe32bdf57419be2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567430"
---
# <span data-ttu-id="6bb86-101">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="6bb86-101">Get-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="6bb86-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6bb86-102">SYNOPSIS</span></span>
<span data-ttu-id="6bb86-103">Получает список хранилищ служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="6bb86-103">Gets a list of Recovery Services vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6bb86-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6bb86-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesVault [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6bb86-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6bb86-105">DESCRIPTION</span></span>
<span data-ttu-id="6bb86-106">Командлет **Get-AzureRmRecoveryServicesVault** получает список хранилищ служб восстановления в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="6bb86-106">The **Get-AzureRmRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="6bb86-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6bb86-107">EXAMPLES</span></span>

### <span data-ttu-id="6bb86-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6bb86-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesVault
```

<span data-ttu-id="6bb86-109">Получение списка хранилищ в выбранной подписке.</span><span class="sxs-lookup"><span data-stu-id="6bb86-109">Get the list of vault in selected subscription.</span></span>

### <span data-ttu-id="6bb86-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6bb86-110">Example 2</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

<span data-ttu-id="6bb86-111">Получение списка хранилищ в группе ресурсов в выбранной подписке.</span><span class="sxs-lookup"><span data-stu-id="6bb86-111">Get the list of vault in resource group in selected subscription.</span></span>

### <span data-ttu-id="6bb86-112">Пример 3</span><span class="sxs-lookup"><span data-stu-id="6bb86-112">Example 3</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
```

<span data-ttu-id="6bb86-113">Получение хранилища в группе ресурсов с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="6bb86-113">Get the vault in resource group with given name.</span></span>

## <span data-ttu-id="6bb86-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6bb86-114">PARAMETERS</span></span>

### <span data-ttu-id="6bb86-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6bb86-115">-Name</span></span>
<span data-ttu-id="6bb86-116">Указывает имя хранилища для запроса.</span><span class="sxs-lookup"><span data-stu-id="6bb86-116">Specifies the name of the vault to query for.</span></span>

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

### <span data-ttu-id="6bb86-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bb86-117">-ResourceGroupName</span></span>
<span data-ttu-id="6bb86-118">Указывает имя группы ресурсов Azure, в которой нужно создать или из которой нужно получить указанный объект служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="6bb86-118">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

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

### <span data-ttu-id="6bb86-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bb86-119">-DefaultProfile</span></span>
<span data-ttu-id="6bb86-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6bb86-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6bb86-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bb86-121">CommonParameters</span></span>
<span data-ttu-id="6bb86-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6bb86-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bb86-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bb86-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bb86-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6bb86-124">INPUTS</span></span>

### <span data-ttu-id="6bb86-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="6bb86-125">None</span></span>
<span data-ttu-id="6bb86-126">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="6bb86-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6bb86-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6bb86-127">OUTPUTS</span></span>

### <span data-ttu-id="6bb86-128">System. Collections. Generic. List ' 1 [Microsoft. Azure. RecoveryServices. ARSVault]</span><span class="sxs-lookup"><span data-stu-id="6bb86-128">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.RecoveryServices.ARSVault]</span></span>

## <span data-ttu-id="6bb86-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="6bb86-129">NOTES</span></span>

## <span data-ttu-id="6bb86-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6bb86-130">RELATED LINKS</span></span>

[<span data-ttu-id="6bb86-131">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="6bb86-131">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="6bb86-132">New-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="6bb86-132">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="6bb86-133">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="6bb86-133">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


