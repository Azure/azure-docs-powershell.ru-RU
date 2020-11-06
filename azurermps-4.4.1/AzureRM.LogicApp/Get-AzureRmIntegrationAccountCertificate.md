---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: C0086E73-CCB1-4B75-B367-C79E17738122
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountCertificate.md
ms.openlocfilehash: 3d26bca20befc31edfa437c7d3f9bc5dfced2b7b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559747"
---
# <span data-ttu-id="502b6-101">Get-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="502b6-101">Get-AzureRmIntegrationAccountCertificate</span></span>

## <span data-ttu-id="502b6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="502b6-102">SYNOPSIS</span></span>
<span data-ttu-id="502b6-103">Получает сертификаты учетной записи интеграции из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="502b6-103">Gets integration account certificates from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="502b6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="502b6-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountCertificate [-ResourceGroupName <String>] [-Name <String>]
 [-CertificateName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="502b6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="502b6-105">DESCRIPTION</span></span>
<span data-ttu-id="502b6-106">Командлет **Get-AzureRmIntegrationAccountCertificate** получает сертификаты учетной записи интеграции из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="502b6-106">The **Get-AzureRmIntegrationAccountCertificate** cmdlet gets integration account certificates from a resource group.</span></span>
<span data-ttu-id="502b6-107">Укажите имя учетной записи интеграции, имя группы ресурсов и имя сертификата.</span><span class="sxs-lookup"><span data-stu-id="502b6-107">Specify the integration account name, resource group name, and certificate name.</span></span>

<span data-ttu-id="502b6-108">Этот модуль поддерживает динамические параметры.</span><span class="sxs-lookup"><span data-stu-id="502b6-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="502b6-109">Чтобы использовать динамический параметр, введите его в командную команду.</span><span class="sxs-lookup"><span data-stu-id="502b6-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="502b6-110">Чтобы найти имена динамических параметров, введите дефис (-) после имени командлета, а затем несколько раз нажмите клавишу TAB, чтобы просмотреть все доступные параметры.</span><span class="sxs-lookup"><span data-stu-id="502b6-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="502b6-111">Если вы не пропустите требуемый параметр шаблона, командлет предложит вам указать значение.</span><span class="sxs-lookup"><span data-stu-id="502b6-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="502b6-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="502b6-112">EXAMPLES</span></span>

### <span data-ttu-id="502b6-113">Пример 1: получение сертификата учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="502b6-113">Example 1: Get an integration account certificate</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01"
Id                : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegartionAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SusbcriptionId/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/<name>
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="502b6-114">Эта команда получает сертификат учетной записи интеграции с именем IntegrationAccountCertificate01.</span><span class="sxs-lookup"><span data-stu-id="502b6-114">This command gets the integration account certificate named IntegrationAccountCertificate01.</span></span>

### <span data-ttu-id="502b6-115">Пример 2: получение сертификатов учетной записи интеграции по имени учетной записи интеграции</span><span class="sxs-lookup"><span data-stu-id="502b6-115">Example 2: Get integration account certificates by integration account name</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegartionAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SusbcriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/<name>
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="502b6-116">Эта команда получает сертификаты учетной записи интеграции для учетной записи интеграции с именем IntegrationAccount31.</span><span class="sxs-lookup"><span data-stu-id="502b6-116">This command gets the integration account certificates for the  integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="502b6-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="502b6-117">PARAMETERS</span></span>

### <span data-ttu-id="502b6-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="502b6-118">-CertificateName</span></span>
<span data-ttu-id="502b6-119">Указывает имя сертификата учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="502b6-119">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="502b6-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="502b6-120">-Name</span></span>
<span data-ttu-id="502b6-121">Указывает имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="502b6-121">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="502b6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="502b6-122">-ResourceGroupName</span></span>
<span data-ttu-id="502b6-123">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="502b6-123">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="502b6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="502b6-124">-DefaultProfile</span></span>
<span data-ttu-id="502b6-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="502b6-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="502b6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="502b6-126">CommonParameters</span></span>
<span data-ttu-id="502b6-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="502b6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="502b6-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="502b6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="502b6-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="502b6-129">INPUTS</span></span>

## <span data-ttu-id="502b6-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="502b6-130">OUTPUTS</span></span>

### <span data-ttu-id="502b6-131">Microsoft. Azure. Management. Logic. Models. IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="502b6-131">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="502b6-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="502b6-132">NOTES</span></span>

## <span data-ttu-id="502b6-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="502b6-133">RELATED LINKS</span></span>

[<span data-ttu-id="502b6-134">New-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="502b6-134">New-AzureRmIntegrationAccountCertificate</span></span>](./New-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="502b6-135">Remove-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="502b6-135">Remove-AzureRmIntegrationAccountCertificate</span></span>](./Remove-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="502b6-136">Set-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="502b6-136">Set-AzureRmIntegrationAccountCertificate</span></span>](./Set-AzureRmIntegrationAccountCertificate.md)


